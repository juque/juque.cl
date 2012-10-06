---
layout: default
title: juque.cl 
---

### Log

{% for post in site.posts %}

* {{ post.date | localize: "%e de %B, %Y"  }} [{{ post.title }}]({{ post.url }} "{{ post.title }}")

{% endfor %}
