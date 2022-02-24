---
layout: default
title: Inpaklijst
parent: Lijsten
---

Inpakken. Nooit leuk en het wordt nog erger als je dingen vergeet. Daarom hier een voorzet. Eerst een algemene lijst en dan onderaan nog wat specifieke lijsten. Je hebt immers niets aan een snowboard tijdens je weekend fietsen in de Ardennen.

# Inpaklijsten

{: .no_toc }

* TOC
{:toc}

{% for inpakCategorie in site.data.inpaklijst.categorieen %}

## {{ inpakCategorie.naam }}

{% for inpakitem in inpakCategorie.items %} - [ ] {{ inpakitem }}
{% endfor %}
{% for inpakSubcategorie in inpakCategorie.subcategorieen %}

### {{ inpakSubcategorie.naam }}

{% for subcategorieitem in inpakSubcategorie.items %} - [ ] {{ subcategorieitem }}
{% endfor %}
{% endfor %}
{% endfor %}
