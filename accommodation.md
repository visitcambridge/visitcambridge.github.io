---
layout: home
permalink: /accommodation/
title: "Staying in Cambridge"
---
<div class="loading">
	<h2>Loading...</h2>
</div> 

<div id="accommodation_map">
	<ins class="bookingaff" data-aid="2093977" data-target_aid="2093977" data-prod="map" data-width="100%" data-height="590" data-lang="ualng" data-dest_id="0" data-dest_type="landmark" data-latitude="52.2046942" data-longitude="0.1191664" data-mwhsb="0" data-address="Cambridge CB2 3AD, UK">
	    <!-- Anything inside will go away once widget is loaded. -->
	     <a href="//www.booking.com?aid=2093977">Booking.com</a>
	</ins>
</div>

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