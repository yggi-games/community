---
categories:
  - table top rpg
---

{% for category in page.categories %}
## {{ category }}


{% for project in site.projects | where_exp:"item","item.categories contains category" %}
### [{{ post.title }}](https://{% if post.source.type == 'gist' %}gist.{% endif %}github.com/{{ post.source.owner }}/{{ post.source.repo}})


{{ post.content }}


{% for tag in post.tags %}
* {{ tag }}
{% endfor %}
{% endfor %}
{% endfor %}
