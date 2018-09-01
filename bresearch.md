---
bg: "research.jpg"
layout: page
permalink: /categories/
title: "Research"
crawlertitle: "Research Projects and Papers"
summary: "Find my recent research projects here:"
active: research
---

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% for post in site.categories[category_name]: 5 %}
   {% if post.welcome %} {% else %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
{% endif %}
    {% endfor %}
  </div>
{% endfor %}
{% for post in site.posts %}

  <article class="index-page">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    {{ post.excerpt }}
  </article>

{% endfor %}
</div>
