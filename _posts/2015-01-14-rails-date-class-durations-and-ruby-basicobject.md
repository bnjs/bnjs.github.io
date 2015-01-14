---
layout: share-post
title: Rails 4.1 Date class, durations, Ruby inheritance, and BasicObject
---

<style>
code { color: crimson; }
pre code { color: inherit; }
</style>

Once in a while working with Rails we encounter something that makes us scratch our heads. When this happens, I make a point to try to figure it out. There is a lot to be learned in the process.

In this adventure, [David](https://twitter.com/davidstosik) stumbles upon some strange Rails behavior and together we investigate.

---

## Rails 4.1 Date class

There is some strange behavior involving Rails `Date` class and durations like `1.day`.

    > Date.current + 1.day
    => 2015-01-15

    > 1.day
    => 86400

    > Date.current + 86400
    => 2251-08-05

Adding `1.day` to the current date returns tomorrow's date, as expected. `1.day` returns `86400` the number of seconds in a day. But adding `86400` to the current date returns the date 86,400 days from today. WTF?

They must be different classes?

    > 1.day.class
    => Fixnum

    > 86400
    => Fixnum

No, they're both `Fixnum`. How does `Date#+` know the difference?

    # rails/activesupport/lib/active_support/core_ext/date/calculations.rb
    class Date
      ...
      def plus_with_duration(other) #:nodoc:
        if ActiveSupport::Duration === other
          other.since(self)
        else
          plus_without_duration(other)
        end
      end
      alias_method :plus_without_duration, :+
      alias_method :+, :plus_with_duration
      ...
    end

[https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/core_ext/date/calculations.rb#L88](https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/core_ext/date/calculations.rb#L88)

So Rails' `Date#+` (`Date#plus_with_duration`) has special handling for `ActiveSupport::Duration` instances, and everything else goes to default Ruby `Date#+`.

But `1.day.class` is a `Fixnum`, right?

    > 1.day.class
    => Fixnum

    > 1.day.is_a? ActiveSupport::Duration
    => true

Apparently it's also an `ActiveSupport::Duration`.

---

## ActiveSupport::Duration

Why is `1.day` a `Fixnum` as well as an `ActiveSupport::Duration`? Does `Duration` inherit from `Fixnum`, or override `#class`?

[https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/duration.rb](https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/duration.rb)

Neither. It inherits from `ProxyObject`. Hmm, this looks like something:

    # rails/activesupport/lib/active_support/duration.rb
    module ActiveSupport
      ...
      class Duration < ProxyObject
        attr_accessor :value, :parts

        def initialize(value, parts) #:nodoc:
          @value, @parts = value, parts
        end
        ...
        private

            def method_missing(method, *args, &block) #:nodoc:
              value.send(method, *args, &block)
            end
      end
    end

[https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/duration.rb](https://github.com/rails/rails/blob/4-1-stable/activesupport/lib/active_support/duration.rb)

If a method is missing, it calls that method on `@value`, which would be a `Fixnum`.

That makes sense. But why would `#class` be missing? All objects respond to `#class`. Isn't `Duration` an `Object`?

    > 1.day.is_a?(Object)
    => true

At first glance, yes, but upon closer inspection, not really...

    > ActiveSupport::Duration.superclass
    => ActiveSupport::ProxyObject

    > ActiveSupport::ProxyObject.superclass
    => BasicObject

    > BasicObject.superclass
    => nil

Actually `Duration` does not inherit `Object`, `@value` does, and `Duration#is_a?` delegates to `@value.is_a?`.

    # rails/activesupport/lib/active_support/duration.rb
    module ActiveSupport
      ...
      class Duration < ProxyObject
        ...
        def is_a?(klass) #:nodoc:
          Duration == klass || value.is_a?(klass)
        end
        ...
      end
    end

So `ActiveSupport::Duration` inherits from `ActiveSupport::ProxyObject` which inherits from `BasicObject` which inherits from nothing. An `ActiveSupport::Duration` is technically not an `Object`.

---

## BasicObject

So what is a `BasicObject`?

> "BasicObject is the parent class of all classes in Ruby. It's an explicit blank class."

[http://ruby-doc.org/core-2.2.0/BasicObject.html](http://ruby-doc.org/core-2.2.0/BasicObject.html)

It's a blank class.

    > BasicObject.new.class
    NoMethodError: undefined method `class' for #<BasicObject:0x007ff3927616b8>
    from (pry):40:in `<main>'

Indeed, it doesn't even respond to `#class`. That explains why `Duration#class` hits `method_missing` and returns `Fixnum`.

The End.

---

**NOTE**: In Rails 4.2, `ActiveSupport::Duration` does not inherit `ActiveSupport::ProxyObject` thus not a `BasicObject`, and `1.day.class` returns `ActiveSupport::Duration`.


*Published January 14, 2015*
