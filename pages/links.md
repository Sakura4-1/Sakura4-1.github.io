---
layout: page
title: 心情
---
<div class="page page-mood">
  {%- for category in site.categories %}
  <div class="list-post">
    <h2 id="{{ category[0] }}">{{ category[0] }}</h2>
    <ul>
      {%- for post in category[1] %}
      <li>
        <span class="date">{{ post.date | date: "%Y/%m/%d" }}</span>
        <div class="title">
          <a href="{{ site.baseurl | append: post.url }}" class="hover-underline">{{ post.title }}</a>
        </div>
      </li>
      {%- endfor %}
    </ul>
  </div>
</div>
