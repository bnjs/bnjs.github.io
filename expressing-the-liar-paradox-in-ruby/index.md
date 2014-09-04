---
layout: default
---

# Expressing the Liar Paradox in Ruby

I was reading about the [Liar paradox](http://en.wikipedia.org/wiki/Liar_paradox) and thought it might be interesting to try to evaluate it as a Ruby expression. The Liar paradox is usually expressed in English with something like:

> "This sentence is false."

The reason it's called a paradox is:

> If "This sentence is false." is true, then the sentence is false, but then if "This sentence is false." is false, then the sentence is true, and so on.

You can read more about it on the [Wikipedia article](http://en.wikipedia.org/wiki/Liar_paradox).

So the most literal way to express the sentence in Ruby would be:

    this_sentence == false

This of course raises:

    NameError: undefined local variable or method `this_sentence'

Ruby doesn't know what `this_sentence` is, so it can't evaluate it. But really we do know what "this sentence" is. It's the sentence. "This sentence" is "This sentence is false." The sentence is, the sentence is false. Sounds kind of like a method definition doesn't it? Let's define it for Ruby:

    def this_sentence
      this_sentence == false
    end

Now what do we get?

    > this_sentence == false
    SystemStackError: stack level too deep

So it seems to me that the Liar paradox expressed in Ruby (and most other programming languages) is just a recursive method that doesn't terminate, causing an infinite loop. It can't be evaluated.

From what I've read about the Liar paradox in the field of logic, for some reason the problem doesn't seem to be quite that simple to resolve. Why is that? I don't know, I'm not a logician. Maybe someone can shed light on this in the comments.
