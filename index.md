---
---
{% for category in site.categories %}
## {{ category[0] }}


{% for post in category[1] %}
### [{{ post.title }}](https://{% if post.source.type == 'gist' %}gist.{% endif %}github.com/{{ post.source.owner }}/{{ post.source.repo }}) 


{{ post.content }}


{% for tag in post.tags %}
* {{ tag }}
{% endfor %}
{% endfor %}
{% endfor %}
