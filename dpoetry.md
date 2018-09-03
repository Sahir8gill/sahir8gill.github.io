---
bg: "rose.jpg"
layout: page
title: "Poetry"
crawlertitle: "A collection of my poems"
permalink: /Poetry/
summary: "A collection of my poems"
active: Poetry
---

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% for post in site.categories[category_name]: 5 %}
   {% if post.welcome %} {% else %}
    <article class="index-page">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
      {{ post.excerpt }}
    </article>
{% endif %}
    {% endfor %}
  </div>
{% endfor %}
</div>

My poetry blog was earlier on Tumblr under [Undefined](https://pictureofprinceparadox.tumblr.com/ "Blog"){:target="_blank"}, but I've combined it with my Mathematical website for ease of access.