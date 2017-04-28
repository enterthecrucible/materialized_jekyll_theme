---
layout: page
title: 
redirect_from:
  - /sistemidiriferimento.html
---

<!-- <div class="row"><div class="col s12 aisf darken-2 white-text" style="border-radius: 4px;"><p>Stiamo importando i post dalla vecchia piattaforma. Al momento i post più vecchi non sono ancora accessibili, ci scusiamo per il disagio.</p></div></div> -->

<!--<ul class="post-list">
  {% for post in site.articolicls %}
  <li>
    <h2>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    {% if post.date %}<div class="chip"><span class="post-meta">{{ post.date | date: "%-d %b %Y" }}</span></div>{% endif %}
    {% if post.author %}<div class="chip"><span class="post-meta">{{ post.author }}</span></div>{% endif %}
    {% if post.categories %}{% for category in post.categories %}{% if category == 'articolicl' %}{% else %}<div class="chip"><span class="post-meta">{{ category }}</span></div>{% endif %}{% endfor %}{% endif %}
    </h2>
    <div class="entry-content">{{ post.excerpt | strip_html }}</div>
  </li>
  <div class="divider"></div>
  {% endfor %}
  </ul> -->

<ul class="post-list">
  {% for post in site.categories.sistemidiriferimento %}
  <li>
    <h2>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
          {{ post.title }}
      </a>
    {% if post.date %}
        <div class="chip">
            <span class="post-meta">
                {{ post.date | date: "%-d %b %Y" }}
            </span>
        </div>
    {% endif %}
    {% if post.author %}
        <div class="chip">
            <span class="post-meta">
                {{ post.author }}
            </span>
        </div>
    {% endif %}
    {% if post.categories %}
        {% for category in post.categories %}
            {% if category == 'sistemidiriferimento' %}
            {% else %}
                <div class="chip">
                    <span class="post-meta">
                        {{ category }}
                    </span>
                </div>
            {% endif %}
        {% endfor %}
    {% endif %}
    </h2>
    <div class="entry-content">
        {{ post.excerpt | strip_html }}
    </div>
  </li>
  <div class="divider"></div>
  {% endfor %}
 </ul>
