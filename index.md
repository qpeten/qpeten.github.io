{% for post in paginator.posts %}
    {{ post.title }}
    {{ post.content }}
{% endfor %}

