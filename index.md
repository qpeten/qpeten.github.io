---
layout: default
---

La dernière mise à jour du site date du {{ site.lastupdate }} 

*****

{% for page in site.pages %}
## [{{ page.title }}]({{ page.url }})
{% if post.content contains '<!--more-->' %}
 {{ post.content | split:'<!--more-->' | first }}
{% else %}
 {{ post.excerpt }}
{% endif %}
{% endfor %}
