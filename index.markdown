---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="atf">
	<div id="atf-wrapper">
		<img id="rc" class="profile-image" src="/assets/images/river-cam.jpg" loading="lazy" alt="Visit Cambridge Official Walking Tours | River Cam" title="Visit Cambridge Official Walking Tours | River Cam">
		<img id="kcc" class="profile-image" src="/assets/images/kings-college-chapel.jpg" loading="lazy" alt="Visit Cambridge Official Walking Tours | Kings College Chapel" title="Visit Cambridge Official Walking Tours | Kings College Chapel">
		<div id="atf-copy">
			<div id="key-messaging-container">
				<h1 class="key-messaging">Official walking tours of Cambridge</h1>
			</div>
			{% include button.html %}
			<img id="mobile" class="profile-image" src="/assets/images/mobile.png" alt="Visit Cambridge Official Walking Tours | Essential sights" loading="eager" title="Visit Cambridge Official Walking Tours | Essential sights">
			<p id="covid" class="description primary-color"><b>COVID-19:</b> We're open for business with socially distanced tours.</p>
		</div>
		<div id="atf-images">
			<img id="bridge-of-sighs" class="profile-image" src="/assets/images/bridge-of-sighs.jpg" loading="eager" alt="Visit Cambridge Official Walking Tours | Bridge of Sighs" title="Visit Cambridge Official Walking Tours | Bridge of Sighs">
		</div>
	</div>
</div>

<div id="experts-container">
	<img class="iotg" src="/assets/images/ta.svg" loading="lazy" alt="Rated 4.5 stars on average on Tripadvisor" title="Rated 4.5 stars on average on Tripadvisor">
	<img class="vc-grey" src="/assets/images/vc-grey.svg" loading="lazy" alt="Quality-assured by Visit Cambridge Ltd" title="Quality-assured by Visit Cambridge Ltd">
	<img class="iotg" src="/assets/images/iotg.svg" loading="lazy" alt="Registered with the Institute of Tourist Guiding" title="Registered with the Institute of Tourist Guiding">
</div>

<div id="guides-container">
	<div id="guides">
		<div class="profile">
			<h2>Our guides</h2>
			<p class="description">Our community of award-winning Green and Blue Badge Guides love Cambridge and can’t wait to share it with you.</p><p>They will tailor your experience to your needs and interests, and no two tours are the same. Green and Blue Badge Guides are accredited by the Institute of Tourist Guiding.</p>
		</div>
		<img id="max" class="profile-image" src="/assets/images/max.jpg" loading="lazy" alt="Visit Cambridge Official Walking Tours | Our guides" title="Visit Cambridge Official Walking Tours | Our guides">
	</div>
</div>

<div id="quote-container">
	<div id="quotes-header"><h3>What guests are saying</h3></div>
	<div id="quote-1" class="quote">
		<p>Don't miss this excellent overview of the town! There is so much history here it is incredible.</p>
	</div>
	<div id="quote-2" class="quote">
		<p>Max made the two hours simply fly. He was full of interesting facts and gave an excellent tour!</p>
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
		<a class="primary-color" href="/feed">See more articles</a>
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