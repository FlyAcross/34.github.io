---
layout: page
title: "Archive"
description: "你看到的，是我练习千字文的所有文章"
header-img: "img/facebook.jpg"
---

<ul class="listing">

{% for post in site.posts %}

  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}

  {% if year != y %}

    {% assign year = y %}
    <h3><li class="listing-seperator">{{ y }}</li></h3>

  {% endif %}

  <li class="listing-item">

    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>

  </li>

{% endfor %}

</ul>
