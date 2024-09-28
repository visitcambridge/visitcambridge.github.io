---
layout: home
permalink: /accommodation/
title: "Stay in Cambridge"
---
<!-- <div class="loading">
	<h2>Loading...</h2>
</div> 
 -->
<!-- <div id="accommodation_map">

</div> -->

<script async src="https://tp.media/content?currency=gbp&trs=352913&shmarker=574778&search_host=search.hotellook.com&locale=en&powered_by=true&draggable=true&disable_zoom=false&show_logo=false&scrollwheel=true&color=%23043F9F&contrast_color=%23ffffff&width=1000&height=500&lat=52.2&lng=0.116667&zoom=13&radius=60&stars=0&rating_from=7&rating_to=10&promo_id=4285&campaign_id=101" charset="utf-8"></script>


<div style="min-height: 35vh;" style="margin-bottom: 100px; margin-top: 60px;">
	<ul class="post-list" >
	  	{%- for post in site.posts -%}
	  		{%- if post.categories contains "accommodation" -%}
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

		(function(d, sc, u) {
		    var s = d.createElement(sc), p = d.getElementsByTagName(sc)[0];
		    s.type = 'text/javascript';
		    s.async = true;
		    s.src = u + '?v=' + (+new Date());
		    p.parentNode.insertBefore(s,p);
		 })(document, 'script', '//aff.bstatic.com/static/affiliate_base/js/flexiproduct.js');

	}, false);
</script>