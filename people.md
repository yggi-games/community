---
social:
  github:
    label: GitHub
    url: https://github.com/%user%
---
{% assign people = site.people %}

{% for person in people %}
  {{ assign s = social.github }}
  [{{ s.label }}]({{ s.url | replace_first:"%user%", person.user }})
  {{ person.content }}
{% endfor %}
