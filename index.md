---
categories:
  - table top rpg
tags:
  - one-shot
  - gm-less
---
{% assign categories = page.categories %}
{% assign tags = page.tags %}

{% for category in categories %}
{% assign projects = site.projects | where_exp:"item","item.categories contains category" %}
{% if projects %}
## {{ category }}


{% for project in projects %}
### [{{ project.title }}](https://{% if project.source.type == 'gist' %}gist.{% endif %}github.com/{{ project.source.owner }}/{{ project.source.repo}})


{{ project.content }}


{% for tag in project.tags %}
{% if tags contains tag %}
* {{ tag }}
{% endif %}
{% endfor %}
{% endfor %}
{% endif %}
{% endfor %}
