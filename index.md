---
layout: default
title: Ben Sullivan
---

<br>
<br>

<div style="margin-left: 50%;">{{ site.time | date: "%B %-d, %Y" }}</div>

<br>
<br>
<br>

Dear Reader:

<br>

Welcome! Allow me to <a href="/about-me">introduce myself</a>.

Below you will find my personal blog, some past and present projects, and some notes about startups.

<br>

## Blog

<p>
{% for post in site.posts %}
{% if post.path contains "_drafts" %}
{% else %}
<span style="white-space:nowrap">{{ post.date | date: "%h %d, %Y" }}</span> <a href="{{ post.url }}">{{ post.title }}</a>
<br>
{% endif %}
{% endfor %}
<span style="white-space:nowrap">Aug 24, 2014</span> <a href="/expressing-the-liar-paradox-in-ruby">Expressing the Liar Paradox in Ruby?</a>
</p>


{% if site.base_url == 'http://localhost:4000' %}
{% for post in site.posts %}
{% if post.path contains "_drafts" %}
<!-- ## <a href="{{ post.url }}" style="color:#f66">{{post.title}}</a> <span>{{ post.date | date: "%h %d, %Y" }}</span> -->
{% else %}
{% endif %}
{% endfor %}
{% endif %}

<br>

## Projects

<!-- a href="https://github.com/bonsaiben/algebra-anki" target="_blank">Algebra Anki</a> - <span>Algebra flashcards for spaced-repetition software Anki</span -->

<p>
<a href="http://dont-kill-the-courier.tumblr.com">Don't Kill the Courier</a> - A blog devoted to typewritten documents from the 1940s, '50s, '60s and '70s<br>
<a href="https://www.tadaku.com" target="_blank">Tadaku</a> - <span>An international cooking lesson service based in Japan</span><br>
<a href="https://tokyo-startup-circle.doorkeeper.jp/" target="_blank">Tokyo Startup Circle</a> - <span>7 people meet over coffee every other Saturday to talk about startups</span><br>
<a href="https://github.com/bonsaiben/bootstrap-snippets" target="_blank">Bootstrap Snippets</a> - <span>Twitter Bootstrap markup snippets for Vim snipMate</span><br>
</p>

<br>

## Notes

<a href="/notes/lists-of-things/">Lists of Things</a>

<a href="/notes/how-to-do-stuff/">How To Do Stuff</a>

<a href="/notes/steve-jobs-10-rules-for-life/">Steve Jobs: 10 Rules for Life</a>

YCombinator

<p>
<a href="/notes/cs183b-lecture-1-dustin-moskovitz-why-to-start-a-startup/">CS183B - Lecture 1: Dustin Moskovitz "Why to Start a Startup" Notes</a><br>
<a href="/notes/sam-altman-ideas-products-teams-and-execution-highlights/">CS183B - Lectures 1+2: Sam Altman "Ideas, Products, Teams and Execution" Notes</a><br>
<a href="/notes/cs183b-lecture-3-paul-graham-counterintuitive-parts-of-startups-and-how-to-have-ideas/">CS183B - Lecture 3: Paul Graham "Counterintuitive Parts of Startups, and How to Have Ideas" Notes</a><br>
<a href="/notes/cs183b-lecture-4-adora-cheung-building-product-talking-to-users-and-growing/">CS183B - Lecture 4: Adora Cheung "Building Product, Talking to Users, and Growing" Notes</a><br>
<a href="/notes/cs183b-lecture-5-peter-thiel-business-strategy-and-monopoly-theory/">CS183B - Lecture 5: Peter Thiel "Business Strategy and Monopoly Theory" Notes</a><br>
<a href="/notes/startup-checklist/">CS183B - Startup Checklist</a><br>
<a href="/2014/09/25/transcript-lecture-1-how-to-start-a-startup/">CS183B - (Transcript) Lecture 1: How to Start a Startup</a><br>
<a href="/transcript-paul-graham-in-conversation-with-nathan-blecharczyk">(Transcript) Paul Graham in Conversation with Nathan Blecharczyk</a>
</p>




<br><br><br><br>
Best,<br><br>
Ben Sullivan
