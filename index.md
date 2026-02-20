---
layout: default
title: Home
---

{% include nav.html %}

# Featured Projects

{% assign items = site.projects | sort: "order" %}

{% for p in items %}
### [{{ p.title }}]({{ site.baseurl }}{{ p.url }})

{% if p.one_liner %}
{{ p.one_liner }}
{% elsif p.subtitle %}
{{ p.subtitle }}
{% endif %}

---
{% endfor %}
