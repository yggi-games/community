---
social:
  - id: github
    label: GitHub
    url: "https://github.com/%user%"
---
{% assign people = site.people %}
{% assign social = page.social %}

{% for person in people %}
## {{ person.name }}
  
  
{{ person.content }}
  
  
### connect
  
  
{% for s in social %}  
* [{{ s.label }}]({{ s.url | replace_first: "%user%", person.social[s.id] }})
{% endfor %}
{% endfor %}
