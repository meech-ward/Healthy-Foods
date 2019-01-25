---
layout: page
title: Recipes
permalink: /recipes
class: recipes
---

<ul class="all-recipes post-list">

  {% assign sorted = site.recipes | sort: 'date' | reverse %}
  {% for post in sorted %}

  {% if post.archived != true %}

    <li>
      <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
      <!-- <p>{{ post.excerpt }}</p> -->
    </li>

  {% endif %}

  {% endfor %}
</ul>