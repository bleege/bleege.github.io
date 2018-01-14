---
layout: page
title: Blog posts by tag 
---

<ul class="tags">
{% assign sorted_tags = site.tags | sort %}
  {% for tag in sorted_tags %}
    {% assign t = tag | first %}
    {% assign posts = tag | last %}

  <li><a href="/tags.html#{{t | downcase | replace:" ","-" }}">{{t | downcase | replace:" ","-" }}</a></li>

  {% endfor %}
</ul>


{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

<h4 id="{{t | downcase | replace:" ","-" }}">{{ t | downcase }}</h4>

<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}