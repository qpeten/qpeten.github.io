---
layout: default
---

This is the index page.
{{site}}
{% for post in site.posts %}
    {{ post.title }}
    {{ post.content }}
{% endfor %}

