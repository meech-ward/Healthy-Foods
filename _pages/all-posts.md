---
layout: page
title: Blog
permalink: /blog
class: blog
---

<ul class="all-posts post-list">

  {% assign sorted = site.blog | sort: 'date' | reverse %}
  {% for post in sorted %}

  {% if post.archived != true %}

    <li>
      <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
      <!-- <p>{{ post.excerpt }}</p> -->
    </li>

  {% endif %}

  {% endfor %}
</ul>