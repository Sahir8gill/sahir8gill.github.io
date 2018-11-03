---
bg: "notes.jpg"
layout: page
title: "Notes&Quotes"
crawlertitle: "Some intersting excerpts from my notes"
permalink: /Notes&Quotes/
summary: "Some interesting excerpts from my notes"
active: Notes&Quotes
---
<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
  {% for post in site.categories[category_name]: 15 %}
   {% if post.welcome %} {% else %}
    {% if post.categories contains "notesandquotes" %}
    <article class="index-page">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
      {{ post.excerpt }}
    </article>
    {% endif %}
  {% endif %}
  {% endfor %}
  </div>
{% endfor %}
</div>