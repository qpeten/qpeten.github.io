---
layout: default
---

This is the index page.

{% for post in paginator.posts %}
    {{ post.title }}
    {{ post.content }}
{% endfor %}

