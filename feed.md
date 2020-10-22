---
layout: home
title: "News and articles"
---
<div style="min-height: 35vh;">
	<ul class="post-list" style="margin-bottom: 100px;">
	  {%- for post in site.posts -%}
	  <li>
	    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
	    <span class="post-meta">{{ post.date | date: date_format }}</span>
	    <h3>
	      <a class="post-link" href="{{ post.url | relative_url }}">
	        {{ post.title | escape }}
	      </a>
	    </h3>
	    {%- if site.show_excerpts -%}
	      {{ post.excerpt }}
	    {%- endif -%}
	  </li>
	  {%- endfor -%}
	</ul>
</div>