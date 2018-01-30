---
layout: doc
title: treehouses.io docs
permalink: /docs
---

asdasd
<ul>
{% for page in site.collections.docs %}
  <li><a href="{{ page.url }}">{{ page.title }}</a></li>
{% endfor %}
</ul>