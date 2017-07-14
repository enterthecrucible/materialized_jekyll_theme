---
layout: en-page
title: Regional Committees
permalink: /en/comitatilocali/
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
				Local Committee of {{ item.nome }}
			</span>
	      	<p>
				President: {{ item.presidente }} 
				<br>
	        	Since: {{ item.fondazione }}
				<br>
				{% if item.ex != nil %}
					Ex presidents: {{ item.ex }}
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
	      		<a href="mailto:{{ item.mail }}&#64;&#97;&#105;&#45;&#115;&#102;&#46;&#105;&#116;" title="Indirizzo email">
					<i class="fa fa-lg fa-envelope"></i>
				</a>
			</div>
	    </li>
	{% endfor %}
</ul>

