---
layout: default
---

{% for page in site.posts %}
<strong><a href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a></strong>
<span>on {{ page.date | date: "%B %e, %Y" }} {% if page.author %} by {{ page.author }}{% endif %}</span>
{% endfor %}