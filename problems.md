---
layout: default
title: Programming Challenges
---

<div id="articles">
  <h1>Programming Challenges </h1>
  <ul class="posts noList">
    {% for post in site.posts %}
        {% if post.category contains 'problems' %}
      <li>
      	<span class="date">{{ post.date | date_to_string }}</span>
      	<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      	<p class="description">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{% endif %}</p>
      </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>
