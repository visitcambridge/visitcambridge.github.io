---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="atf">
	<div id="atf-wrapper">
		<img id="rc" class="profile-image" src="/assets/images/river-cam.jpg" loading="lazy" alt="Visit Cambridge Ltd | River Cam" title="Visit Cambridge Ltd | River Cam">
		<img id="kcc" class="profile-image" src="/assets/images/kings-college-chapel.jpg" loading="lazy" alt="Visit Cambridge Ltd | Kings College Chapel" title="Visit Cambridge Ltd | Kings College Chapel">
		<div id="atf-copy">
			<div id="key-messaging-container">
				<h1 class="key-messaging">Discover the best of Cambridge</h1>
			</div>
			{% include button.html %}
			<img id="mobile" class="profile-image" src="/assets/images/mobile.png" alt="Visit Cambridge Ltd | Essential sights" loading="eager" title="Visit Cambridge Ltd | Essential sights">
			<p id="covid" class="description primary-color"><b>COVID-19:</b> Please follow local guidelines whilst visiting.</p>
		</div>
		<div id="atf-images">
			<img id="bridge-of-sighs" class="profile-image" src="/assets/images/bridge-of-sighs.jpg" loading="eager" alt="Visit Cambridge Ltd | Bridge of Sighs" title="Visit Cambridge Ltd | Bridge of Sighs">
		</div>
	</div>
</div>

<div id="experts-container">
	<img class="iotg" src="/assets/images/ta.svg" loading="lazy" alt="Rated 4.5 stars on average on Tripadvisor" title="Rated 4.5 stars on average on Tripadvisor">
	<img class="vc-grey" src="/assets/images/vc-grey.svg" loading="lazy" alt="Quality-assured by Visit Cambridge Ltd" title="Quality-assured by Visit Cambridge Ltd">
</div>

<div id="guides-container">
	<div id="guides">
		<div id="profile">
			<h2>Virtual Cambridge</h2>
			<p class="description">Since lock down, its been hard to visit Cambridge - until NOW! The David Parr house are running virtual tours of this iconic house.</p><p>Join a Zoom call with a difference where their guides gives you a 3D tour around 186 Gwydir Street.</p>
			<a class="button-anchor secondary-button" href="https://davidparrhouse.org/product/online-tour/"><div class="button noselect">Book a virtual tour</div></a>
		</div>
		<img id="max" class="profile-image" src="/assets/images/david-parr.png" loading="lazy" alt="Virtual Tour of David Parr House" title="David Parr House | Vitual Tour">
	</div>
</div>


<div id="guides-container">
	<div id="guides">
		<div class="profile">
			<h2>Cambridge tours</h2>
			<p class="description">We've partnered with award-winning providers to offer tours and activites that showcase the best of Cambridge. When you visit Cambridge, you'll be greeted by guides that love the area and can’t wait to share its history with you.</p><p>They can tailor your experience to your needs and interests, and no two tours are the same.</p>
		</div>
		<img id="max" class="profile-image" src="/assets/images/max.jpg" loading="lazy" alt="Visit Cambridge Ltd | Our guides" title="Visit Cambridge Ltd | Official tours">
	</div>
</div>

<div id="quote-container">
	<div id="quotes-header"><h3>What guests are saying</h3></div>
	<div id="quote-1" class="quote">
		<p>Don't miss this excellent overview of the town! There is so much history here it is incredible.</p>
	</div>
	<div id="quote-2" class="quote">
		<p>Our guide made the time simply fly. He was full of interesting facts and gave an excellent tour!</p>
	</div>
	<div id="quote-3" class="quote">
		<p>I was born in Cambridge, but I learned more about it in these two hours than during my lifetime.</p>
	</div>
</div>

{%- if site.posts.size > 0 -%}
	<div id="news-container">
		<div id="news-header"><h2>News and articles</h2></div>
        <ul class="post-list">
		  	{%- for post in site.posts -%}
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
		  	{%- endfor -%}
        </ul>
		<a class="secondary-font-color" href="/feed">See more articles</a>
	</div>
{%- endif -%}

<script>
	var footerButton = function() {

		var footer = document.getElementById('sticky-footer');
	    var buttonContainer = document.querySelector('#atf-copy');
		var button = buttonContainer.querySelector('.primary-button');
	    var buttonOffset = button.getBoundingClientRect();
	    var triggerHeight = window.pageYOffset + buttonOffset.top + buttonOffset.height*.6;
	    footer.classList.remove("show-footer");
		window.onscroll = function() {
		    if (window.pageYOffset > triggerHeight || window.innerWidth < 480) {
		        footer.classList.add("show-footer");
		    } else {
		        footer.classList.remove("show-footer");
		    }
		}
		// window.smoothScroll = function(target) {
		//     var scrollContainer = target;
		//     do { //find scroll container
		//         scrollContainer = scrollContainer.parentNode;
		//         if (!scrollContainer) return;
		//         scrollContainer.scrollTop += 1;
		//     } while (scrollContainer.scrollTop == 0);

		//     var targetY = 0;
		//     do { //find the top of target relatively to the container
		//         if (target == scrollContainer) break;
		//         targetY += target.offsetTop;
		//     } while (target = target.offsetParent);

		//     scroll = function(c, a, b, i) {
		//         i++; if (i > 30) return;
		//         c.scrollTop = a + (b - a) / 30 * i;
		//         setTimeout(function(){ scroll(c, a, b, i); }, 20);
		//     }
		//     // start scrolling
		//     scroll(scrollContainer, scrollContainer.scrollTop, targetY, 0);
		// }

		// window.openBookingPortal = (function() {
		// 	var opened = false;
		// 	return function() {
		//         if (!opened) {
		//             opened = true;
		//             var tag = document.createElement("script");
		// 			tag.setAttribute("async", "");
		// 			tag.setAttribute("defer", "");
		// 			tag.src = "https://widgets.bokun.io/assets/javascripts/apps/build/BokunWidgetsLoader.js?bookingChannelUUID=b2a94f77-29a2-4342-86ca-10ac40ad7626";
		// 			document.getElementsByTagName("head")[0].appendChild(tag);
		//         }
		//     };
		// })();

		//    var guides = document.getElementById('guides-header');
		//    var guidesOffset = guides.getBoundingClientRect();
		//    var triggerHeight = window.pageYOffset + guidesOffset.top + guidesOffset.height*.6;
		// window.onscroll = function() {
		//     if (window.pageYOffset > triggerHeight) {
		//         openBookingPortal();
		//     }
		// }

	};

	window.addEventListener('DOMContentLoaded', footerButton, false);
	window.addEventListener('resize', footerButton, false);
</script>