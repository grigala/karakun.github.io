---
layout: page
title: Talks
permalink: /talks/
---
Overview of talks that were done by members of Karakun:
{% for talk in site.data.talks %}
<p>
{% assign author = site.people | where:'name', talk.author | first %}
<h3>{{ talk.name }} - {{ talk.lectures[0].conference }} {{ talk.lectures[0].year }}</h3>
<p>{{ talk.summary }}</p>
<p>Author: <a href="{{ author.url }}">{{ author.firstName }} {{ author.lastName }}</a></p>
</p>
{% endfor %}