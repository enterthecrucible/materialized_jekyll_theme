---
layout: page
title: Eventi
permalink: /eventi/
---
{% for event in site.events reversed %}
    {% if event.date < site.time %}
        {% assign nfuturi = forloop.index0 %}
        {% break %}
    {% endif %}
{% endfor %}
{% assign npassati = site.events.size | minus:nfuturi %}

## Prossimamente

{% include eventi_futuri.html %}
    
## Eventi organizzati dai Comitati Locali

{% include eventi_locali.html %}

## Grandi eventi passati

{% include eventi_passati.html %}

{% include eventi_modal.html %}

