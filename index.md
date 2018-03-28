---
layout: default
---

La dernière mise à jour du site date du {{ site.lastupdate }} 

*****

{% for page in site.pages %}
  {% if page.onFrontPage == true %}
    ## [{{ page.title }}]({{ page.url }})
    {% if page.content contains '<!--more-->' %}
      {{ page.content | split:'<!--more-->' | first }}
    {% else %}
      {{ page.content }}
    {% endif %}
  {% endif %}
{% endfor %}
