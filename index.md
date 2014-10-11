---
layout: default
title: Benjamin Sullivan
---

<h2>Hi there. My name's Ben <span class="lowkey">and I build web apps, and help build products, teams, startups, communities.</span></h2>
<h2 class="lowkey">More <a href="/about-me">about me</a></h2>

---

# Writings

{% for post in site.posts %}
{% if post.path contains "_drafts" %}
{% else %}
## [{{ post.title }}]({{ post.url }}) <span class="lowkey">{{ post.date | date: "%h %d, %Y" }}</span>
{% endif %}
{% endfor %}

## [Why I Want an iWatch](/why-i-want-an-iwatch) <span class="lowkey">Sept 4, 2014</span>

## [Expressing the Liar Paradox in Ruby](/expressing-the-liar-paradox-in-ruby) <span class="lowkey">Aug 24, 2014</span>

{% if site.base_url == 'http://localhost:4000' %}
{% for post in site.posts %}
{% if post.path contains "_drafts" %}
## <a href="{{ post.url }}" style="color:#f66">{{post.title}}</a> <span class="lowkey">{{ post.date | date: "%h %d, %Y" }}</span>
{% else %}
{% endif %}
{% endfor %}
{% endif %}


---

# Notes

## [CS183B Lecture 5: Peter Thiel "Business Strategy and Monopoly Theory" Notes](/notes/cs183b-lecture-5-peter-thiel-business-strategy-and-monopoly-theory/) <span class="lowkey">WIP</span>

## [CS183B Lecture 4: Adora Cheung "Building Product, Talking to Users, and Growing" Notes](/notes/cs183b-lecture-4-adora-cheung-building-product-talking-to-users-and-growing/) <span class="lowkey">WIP</span>

## [CS183B Lecture 3: Paul Graham "Counterintuitive Parts of Startups, and How to Have Ideas" Notes](/notes/cs183b-lecture-3-paul-graham-counterintuitive-parts-of-startups-and-how-to-have-ideas/) <span class="lowkey">Oct 11, 2014</span>

## [CS183B Lecture 1: Dustin Moskovitz "Why to Start a Startup" Notes](/notes/cs183b-lecture-1-dustin-moskovitz-why-to-start-a-startup/) <span class="lowkey">Oct 11, 2014</span>

## [Startup Checklist](/notes/startup-checklist/) <span class="lowkey">Oct 5, 2014</span>

## [CS183B Lectures 1+2: Sam Altman "Ideas, Products, Teams and Execution" Notes](/notes/sam-altman-ideas-products-teams-and-execution-highlights/) <span class="lowkey">Oct 3, 2014</span>

---

# Projects

<h2>
  <a href="http://www.thebuilding.io" target="_blank">The Building</a>
  <br/>
  <span class="lowkey">Noteworthy news and articles for startup founders and developers</span>
</h2>

<h2>
  <a href="/startup-faq">Startup FAQ</a>
  <br/>
  <span class="lowkey">Insights distilled from top startup articles</span>
</h2>

<h2>
  <a href="/startup-knowledgebase">Startup Knowledgebase</a>
  <br/>
  <span class="lowkey">Categorized collection of insightful articles</span>
</h2>

<h2>
  <a href="http://www.meetup.com/LeanStartupTokyo/" target="_blank">Bootstrap Lunch</a>
  <br/>
  <span class="lowkey">Up to 7 entrepreneurs meet over coffee every other Saturday (founding organizer)</span>
</h2>

<h2>
  <a href="https://kenzai.me" target="_blank">Kenzai</a>
  <br/>
  <span class="lowkey">Online fitness platform based on real food, real exercise and real people (full-stack developer)</span>
</h2>

<h2>
  <a href="https://www.tadaku.com" target="_blank">Tadaku</a>
  <br/>
  <span class="lowkey">Cook real food with real people (co-founded, built)</span>
</h2>

---

# Transcripts

## [Transcript: Lecture 1 - How to Start a Startup](/2014/09/25/transcript-lecture-1-how-to-start-a-startup/)

## [Transcript: Paul Graham in Conversation with Nathan Blecharczyk](/transcript-paul-graham-in-conversation-with-nathan-blecharczyk)

