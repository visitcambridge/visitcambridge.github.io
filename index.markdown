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
			<p class="description primary-color"><b>COVID-19:</b> We're open for business with socially distanced tours.</p>
		</div>
		<div id="atf-images">
			<img id="bridge-of-sighs" class="profile-image" src="/assets/images/bridge-of-sighs.jpg" loading="eager" alt="Visit Cambridge Official Walking Tours | Bridge of Sighs" title="Visit Cambridge Official Walking Tours | Bridge of Sighs">
		</div>
	</div>
</div>

<div id="experts-container">
	<div id="experts-header"><h2>Hosted by award-winning guides</h2></div>
	<img class="iotg" src="/assets/images/ta.svg" loading="lazy" alt="Rated 4.5 stars on average on Tripadvisor" title="Rated 4.5 stars on average on Tripadvisor">
	<img class="vc-grey" src="/assets/images/vc-grey.svg" loading="lazy" alt="Quality-assured by Visit Cambridge Ltd" title="Quality-assured by Visit Cambridge Ltd">
	<img class="iotg" src="/assets/images/iotg.svg" loading="lazy" alt="Registered with the Institute of Tourist Guiding" title="Registered with the Institute of Tourist Guiding">
</div>

<div id="next-up-container">
	<div id="next-up-header"><h2>Our guides</h2></div>
	<div id="next-up">
		<img id="max" class="profile-image" src="/assets/images/max.jpg" alt="Visit Cambridge Official Walking Tours | Our guides" title="Visit Cambridge Official Walking Tours | Our guides">
		<div class="profile">
			<p class="description">Our community of Green and Blue Badge Guides love Cambridge and can’t wait to share it with you. They will tailor your experience to your needs and interests, and no two tours are the same. Green and Blue Badge Guides are accredited by the Institute of Tourist Guiding.</p>
			{% include button.html %}
		</div>
	</div>
</div>

<div id="next-up-container">
	<div id="next-up-header"><h2>Essential Cambridge</h2></div>
	<div id="tour-container">
		<div id="tour-description">
			<p>Join the official walking tour of Cambridge to see its unmissable sights.</p>
			<p>Your 90 minute tour will span Cambridge’s 2,000 year history - from its humble beginnings as an Iron Age camp, to its current status as world-leading centre of learning and research.</p>
			<p>You’ll hear tales of its people and landmarks, including the formation of Cambridge University and its colleges from old religious institutions.</p>
			<p>You’ll visit places that have changed the world, including the Cavendish Laboratory Building which is linked with 29 Nobel Laureates. You’ll see where the very structure of our being, the double helix DNA, was discovered by Watson, Crick, Wilkins, and Franklin.</p>
			<p>Along the way you’ll see:</p>
			<ul>
				<li> King's College, whose world famous Chapel is home to an exceptional choir.</li>
			    <li> Trinity College, where you'll find Newton's apple tree.</li>
			    <li> St John's College, where William Wilberforce started his university career before fighting to abolish slavery.</li>
			</ul>
		</div>
	</div>
</div>

<div id="quote-container">
	<div id="quotes-header"><h3>What our guests are saying</h3></div>
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

<div class="bokunWidget" data-src="https://widgets.bokun.io/online-sales/b2a94f77-29a2-4342-86ca-10ac40ad7626/experience-calendar/423944"></div>
<noscript>Please enable javascript in your browser to book</noscript>

<div style="width:100%; height: 120px;"></div>

<script>
	document.addEventListener('DOMContentLoaded', function() {

		var tag = document.createElement("script");
		tag.setAttribute("async", "");
		tag.setAttribute("defer", "");
		tag.src = "https://widgets.bokun.io/assets/javascripts/apps/build/BokunWidgetsLoader.js?bookingChannelUUID=b2a94f77-29a2-4342-86ca-10ac40ad7626";
		document.getElementsByTagName("head")[0].appendChild(tag);

		window.smoothScroll = function(target) {
		    var scrollContainer = target;
		    do { //find scroll container
		        scrollContainer = scrollContainer.parentNode;
		        if (!scrollContainer) return;
		        scrollContainer.scrollTop += 1;
		    } while (scrollContainer.scrollTop == 0);

		    var targetY = 0;
		    do { //find the top of target relatively to the container
		        if (target == scrollContainer) break;
		        targetY += target.offsetTop;
		    } while (target = target.offsetParent);

		    scroll = function(c, a, b, i) {
		        i++; if (i > 30) return;
		        c.scrollTop = a + (b - a) / 30 * i;
		        setTimeout(function(){ scroll(c, a, b, i); }, 20);
		    }
		    // start scrolling
		    scroll(scrollContainer, scrollContainer.scrollTop, targetY, 0);
		}
	}, false);
</script>