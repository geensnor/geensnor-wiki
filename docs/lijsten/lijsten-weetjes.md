---
title: Weetjes
parent: Lijsten
---

#  Weetjes

{{site.data.weetjes | size}} om precies te zijn.

---

{% assign i = 1 %}

{% for weetje in site.data.weetjes %}
{% increment i %}. {{ weetje | newline_to_br  }}
{% endfor %}
