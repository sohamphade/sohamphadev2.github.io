---
layout: default
title: Archive
---



<!-- 
{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h2>{{ yearMonth.name }}</h2>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url | absolute_url }}/index.html">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %} --->

<!-- {% for post in site.posts %}
<li><a href="{{ post.url | absolute_url }}/index.html">{{ post.title }}</a></li>
{% endfor %} --->




{% for post in site.posts %}
<hr style="height:2px;border-width:0;color:gray;background-color:gray">
<div class="bcolumn">
  <a href="{{ post.url | absolute_url }}index.html" style="text-decoration: none;">
  <article class="post">
  	<h2 class="post-title">{{ post.title }}</h2>
    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">{{ post.date | date_to_string }}</time>
    <h4> {{ post.tagline}} </h4>
    <!--
    {{ post.excerpt | strip_html | append: ''}}
    <a href="{{ post.url | absolute_url }}/index.html">Continue reading</a>
    --->
  </article>
  </a>
</div>
{% endfor %}

