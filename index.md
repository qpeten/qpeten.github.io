---
layout: default
---

La dernière mise à jour du site date du {{ site.lastupdate }} 

*****

{% for page in site.pages %}
## [{{ page.title }}]({{ page.url }})
{% if ppage.content contains '<!--more-->' %}
 {{ page.content | split:'<!--more-->' | first }}
{% else %}
 {{ page.excerpt }}
{% endif %}
{% endfor %}
