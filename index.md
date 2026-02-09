---
layout: default
title: Inici
---

# Cròniques de la Família v2

Benvinguts! Aquesta web recull les cròniques de la família **organitzades per períodes** (cada període correspon a la vida d’un patriarca o matriarca) i per **històries** (fets destacats).

## Períodes

{% assign periodes_ordenats = site.periodes | sort: "inici" %}
<ul>
{% for p in periodes_ordenats %}
  <li>
    <a href="{{ p.url | relative_url }}"><strong>{{ p.nom }}</strong></a>
    <span>({{ p.inici }}–{{ p.fi }})</span>
    {% if p.resum %}<div>{{ p.resum }}</div>{% endif %}
  </li>
{% endfor %}
</ul>

## Últimes històries

{% assign ultimes = site.histories | sort: "data" | reverse %}
<ul>
{% for h in ultimes limit: 8 %}
  <li>
    <a href="{{ h.url | relative_url }}">{{ h.title }}</a>
    <small>— {{ h.data | date: "%d/%m/%Y" }} · {{ h.periode | upcase }}</small>
  </li>
{% endfor %}
</ul>

➡️ Veure la <a href="{{ '/timeline' | relative_url }}">línia temporal</a>.
