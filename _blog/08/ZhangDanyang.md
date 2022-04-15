---
author: "Danyang Zhang"
title: "Draft my personal website"
layout: post
topic: "08"
short-topic: Blogdown...
due-date: 2022-03-24
root: ../../
---

I set up my website using Blogdown. The major problem that I encountered (and I still did not solve) is that I failed to change the avatar of the website. I edited config.toml by changing the path of the image I intend to use within [params.logo]. I tried putting the image into different folders: source/static, [myusername].github.io/static/images, and even set logo = "" to delete the logo, but the initial logo is still there.

I anticipate using this site by putting brief descriptions of my work on it.


{% assign num_posts = site.blog | size %}
{% if num_posts > 0 %}
## Class posts:

<ul>
{% for post in site.blog %}
  {% if page.topic == post.topic %}
  <li><a href="{{ post.url }}">{{ post.title }} by {{ post.author }}</a></li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}
