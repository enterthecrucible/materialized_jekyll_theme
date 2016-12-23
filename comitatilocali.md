---
layout: page
title: Comitati Locali
permalink: /comitatilocali/
redirect_from:
  - /it/20-comitati-locali/
---

{% assign n = 0 %}
{% for item in site.data.LC %}
	{% assign n = n | plus: 1 %}
{% endfor %}

L'AISF conta al momento {{ n }} comitati locali in altrettante università:

<ul class="collection">
	{% for item in site.data.LC %}
	    <li class="collection-item avatar" id="{{ item.nome }}">
	      	<img src="{{ item.img }}" alt="" class="circle">
	      	<span class="title">
				Comitato Locale di {{ item.nome }}
			</span>
	      	<p>
				Presidente: {{ item.presidente }} 
				<br>
	        	Fondazione: {{ item.fondazione }}
				<br>
				{% if item.ex != nil %}
					Ex presidenti: {{ item.ex }}
				{% endif %} 				
	      	</p>
	      	<div class="secondary-content">
				{% if item.fb != nil %}
					<a href="{{ item.fb }}" title="Pagina Facebook">
						<i class="fa fa-lg fa-facebook-square" aria-hidden="true"></i>
					</a>
				{% endif %}
				{% if item.regolamento != nil %}
		        	<a href="{{ item.regolamento }}" title="Regolamento Interno">
						<i class="fa fa-lg fa-file-text"></i>
					</a>
				{% endif %}
	      		<a href="mailto:{{ item.mail }} &#64;&#97;&#105;&#45;&#115;&#102;&#46;&#105;&#116;" title="Indirizzo email">
					<i class="fa fa-lg fa-envelope"></i>
				</a>
			</div>
	    </li>
	{% endfor %}
</ul>


## Provenienza geografica

<a href="/geo/">Qui</a> è possibile trovare ulteriori informazioni sullo storico della provenienza geografica dei membri AISF.

## Formare un nuovo comitato locale

Si faccia riferimento a [questa](/nuovocomitatolocale/) pagina.
