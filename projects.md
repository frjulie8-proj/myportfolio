---
layout: default
title: Projects
---

{% include nav.html %}

# Projects

{% assign items = site.projects | sort: "order" %}

{% for p in items %}
### [{{ p.title }}]({{ site.baseurl }}{{ p.url }})
{{ p.subtitle }}

{% if p.one_liner %}
{{ p.one_liner }}
{% endif %}

---
{% endfor %}
