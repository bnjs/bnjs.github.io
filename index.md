---
layout: default
title: Benjamin Sullivan
---

<h2>Hi there. My name's Ben <span class="lowkey">and I build systems, software, products, and rally teams, startups, communities.</span></h2>
<h2 class="lowkey">
More <a href="/about-me">about me</a>
<div style="float:right;">
<a href="https://twitter.com/bnjs"><i class="fa fa-twitter"></i></a>
&nbsp;&nbsp;
<a href="https://github.com/bonsaiben"><i class="fa fa-github"></i></a>
&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/bnjsu"><i class="fa fa-linkedin"></i></a>
</div>
</h2>

<h2>
</h2>

---

# Blog

{% for post in site.posts %}
{% if post.path contains "_drafts" %}
{% else %}
## [{{ post.title }}]({{ post.url }}) <span class="lowkey" style="color:#ccc;white-space:nowrap">{{ post.date | date: "%h %d, %Y" }}</span>
{% endif %}
{% endfor %}

## [Expressing the Liar Paradox in Ruby?](/expressing-the-liar-paradox-in-ruby) <span class="lowkey" style="color:#ccc;white-space:nowrap">Aug 24, 2014</span>

{% if site.base_url == 'http://localhost:4000' %}
{% for post in site.posts %}
{% if post.path contains "_drafts" %}
## <a href="{{ post.url }}" style="color:#f66">{{post.title}}</a> <span class="lowkey">{{ post.date | date: "%h %d, %Y" }}</span>
{% else %}
{% endif %}
{% endfor %}
{% endif %}

---

# Projects

<h2>
  <a href="https://github.com/bonsaiben/nightlight" target="_blank">Nightlight</a>
  <br/>
  <span class="lowkey"><em>Rails gem</em>, shed light on the dark corners of your app</span>
</h2>

<h2>
  <a href="https://www.tadaku.com" target="_blank">Tadaku</a>
  <br/>
  <span class="lowkey"><em>Service</em>, cook real food with real people (co-founded, built)</span>
</h2>

<h2>
  <a href="http://www.meetup.com/tokyo-startup-circle/" target="_blank">Tokyo Startup Circle</a>
  <br/>
  <span class="lowkey"><em>Event</em>, up to 7 people meet over coffee every other Saturday to discuss startups (founding organizer)</span>
</h2>

<h2>
  <a href="https://github.com/bonsaiben/bootstrap-snippets" target="_blank">Bootstrap Snippets</a>
  <br/>
  <span class="lowkey"><em>Vim plugin</em>, Bootstrap 3.2 markup snippets for Vim snipMate</span>
</h2>
---

# Notes

## CS183B

## [Lecture 1: Dustin Moskovitz "Why to Start a Startup" Notes](/notes/cs183b-lecture-1-dustin-moskovitz-why-to-start-a-startup/)

## [Lectures 1+2: Sam Altman "Ideas, Products, Teams and Execution" Notes](/notes/sam-altman-ideas-products-teams-and-execution-highlights/)

## [Lecture 3: Paul Graham "Counterintuitive Parts of Startups, and How to Have Ideas" Notes](/notes/cs183b-lecture-3-paul-graham-counterintuitive-parts-of-startups-and-how-to-have-ideas/)

## [Lecture 4: Adora Cheung "Building Product, Talking to Users, and Growing" Notes](/notes/cs183b-lecture-4-adora-cheung-building-product-talking-to-users-and-growing/)

## [Lecture 5: Peter Thiel "Business Strategy and Monopoly Theory" Notes](/notes/cs183b-lecture-5-peter-thiel-business-strategy-and-monopoly-theory/)

## [Startup Checklist](/notes/startup-checklist/)

---

# Transcripts

## [Transcript: Lecture 1 - How to Start a Startup](/2014/09/25/transcript-lecture-1-how-to-start-a-startup/)

## [Transcript: Paul Graham in Conversation with Nathan Blecharczyk](/transcript-paul-graham-in-conversation-with-nathan-blecharczyk)

