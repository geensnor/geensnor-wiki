---
title: Haiku's
parent: Lijsten
---

# Haiku's

Kleine Japanse gedichtjes met 17 lettergrepen.

---

{% for haiku in site.data.haiku %}
{{ haiku | newline_to_br  }}
{% endfor %}