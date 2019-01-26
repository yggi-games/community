---
categories:
  - table top rpg
---

{% for category in page.categories %}
{% assign projects = site.projects | where_exp:"item","item.categories contains category" %}
{% if projects %}
## {{ category }}


{% for project in projects %}
### [{{ project.title }}](https://{% if project.source.type == 'gist' %}gist.{% endif %}github.com/{{ project.source.owner }}/{{ project.source.repo}})


{{ project.content }}


{% for tag in project.tags %}
* {{ tag }}
{% endfor %}
{% endfor %}
{% endif %}
{% endfor %}
