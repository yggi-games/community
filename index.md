---
---

{% for category in site.categories %}
## {{ category[0] }}


{% for post in category[1] %}
### [{{ post.title }}]({{ site.github.baseurl }}{{ post.url }})


{% for tag in post.tags %}
* {{ tag }}
{% endfor %}
{% endfor %}
{% endfor %}
