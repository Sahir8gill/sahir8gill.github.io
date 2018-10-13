---
bg: "research.jpg"
layout: page
permalink: /Research/
title: "Research"
crawlertitle: "Research Projects and Papers"
summary: "Find my recent research projects here:"
active: research
---

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% for post in site.categories[category_name]: 15 %}
   {% if post.welcome %} {% else %}
    {% if post.categories contains "research" %}
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