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
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
   {% if post.welcome %} {% else %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
{% endif %}
    {% endfor %}
  </div>
{% endfor %}
</div>