---
layout: home
permalink: /tours/
title: "Activities in Cambridge"
---
<div style="margin-top: -10px; margin-left: -16px; width: calc(100% + 32px);" data-gyg-href="https://widget.getyourguide.com/default/activites.frame" data-gyg-locale-code="en-US" data-gyg-widget="activities" data-gyg-number-of-items="8" data-gyg-excluded-tour-ids="2095,18407,85239" data-gyg-partner-id="4BFP0TS" data-gyg-q="Cambridge"></div>

<div style="min-height: 35vh;" style="margin-bottom: 100px; margin-top: 60px;">
	<ul class="post-list" >
	  	{%- for post in site.posts -%}
	  		{%- if post.categories contains "activities" -%}
			 	<li>
			 		<div class="feed-item">
				 		<div class="feed-body">
						  	{%- if post.author -%}
						    	<p class="post-meta" style="margin-top: 0;">by {{ post.author }}</p>
						    {%- endif -%}
						    
						    <h3 class="feed-title"><a class="post-link" href="{{ post.url | relative_url }}">
						        {{ post.title | escape }}
						    </a></h3>

						    <p class="post-meta post-summary pointer" onclick="location.href='{{ post.url | relative_url }}';">
						    	{%- if post.summary -%}
						    		{{ post.summary }}
						    	{%- else -%}
						    		{{ post.content | strip_html | truncate: 147 }}
						    	{%- endif -%}
						    </p>

						    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
						    <p class="post-meta" style="margin-bottom: 0;">{{ post.date | date: date_format }}</p>
					    </div>
			    	  	<div class="feed-image pointer" onclick="location.href='{{ post.url | relative_url }}';">
			        		<img src="{%- if post.tile_image_url -%}{{ post.tile_image_url }}{%- else -%}{%- endif -%}" loading="lazy" alt="News and articles | {{ post.title | escape }}" title="News and articles | {{ post.title | escape }}">    	
			    	  	</div>
			  		</div>
			  	</li>
			{%- endif -%} 	
	  	{%- endfor -%}
	</ul>
</div>
  
<script>
	document.addEventListener('DOMContentLoaded', function() {

		var tag = document.createElement("script");
		tag.setAttribute("async", "");
		tag.setAttribute("defer", "");
		tag.setAttribute("data-gyg-partner-id", "4BFP0TS");
		tag.src = "https://widget.getyourguide.com/dist/pa.umd.production.min.js"
		document.getElementsByTagName("head")[0].appendChild(tag);

	}, false);
</script>