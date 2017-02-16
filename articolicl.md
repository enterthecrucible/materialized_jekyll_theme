---
layout: page
title: "Articoli Comitati Locali"
redirect_from:
  - /articolicl.html
---

<!-- <div class="row"><div class="col s12 aisf darken-2 white-text" style="border-radius: 4px;"><p>Stiamo importando i post dalla vecchia piattaforma. Al momento i post più vecchi non sono ancora accessibili, ci scusiamo per il disagio.</p></div></div> -->

<ul class="post-list">
  {% for articolocl in site.articolicls %}
  <li>
    <h2>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ articolocl.title }}</a>
    {% if articolocl.date %}<div class="chip"><span class="post-meta">{{ articolocl.date | date: "%-d %b %Y" }}</span></div>{% endif %}
    {% if articolocl.author %}<div class="chip"><span class="post-meta">{{ articolocl.author }}</span></div>{% endif %}
    {% if articolocl.categories %}{% for category in articolocl.categories %}{% if category == 'articolicl' %}{% else %}<div class="chip"><span class="post-meta">{{ category }}</span></div>{% endif %}{% endfor %}{% endif %}
    </h2>
    <div class="entry-content">{{ articolocl.excerpt | strip_html }}</div>
  </li>
  <div class="divider"></div>
  {% endfor %}
  </ul>
