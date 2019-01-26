---
social:
  github:
    label: GitHub
    url: "https://github.com/%user%"
---
{% assign people = site.people %}
{% assign social = page.social %}

{% for person in people %}
  {{ assign s = social.github }}
  [{{ s.label }}]({{ s.url | replace_first: "%user%", person.social.github }})
  {{ social }}
  {{ person.social.github }}
  {{ person.content }}
{% endfor %}
