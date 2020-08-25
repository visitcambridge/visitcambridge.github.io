---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="atf">
	<div id="atf-wrapper">
		<img id="rc" class="profile-image" src="/assets/images/river-cam.jpg" alt="Visit Cambridge Official Walking Tours | River Cam" title="Visit Cambridge Official Walking Tours | River Cam">
		<img id="kcc" class="profile-image" src="/assets/images/kings-college-chapel.jpg" alt="Visit Cambridge Official Walking Tours | Kings College Chapel" title="Visit Cambridge Official Walking Tours | Kings College Chapel">
		<div id="atf-copy">
			<div id="key-messaging-container">
				<h1 class="key-messaging">Official walking tours of Cambridge</h1>
			</div>
			{% include button.html url="https://airtable.com/shrKMvV2iBd4rwRSv" %}
			<p class="description primary-color"><b>COVID-19:</b> We're open for business. All of our tours are socially distanced.</p>
		</div>
		<div id="atf-images">
			<img id="bridge-of-sighs" class="profile-image" src="/assets/images/bridge-of-sighs.jpg" alt="Visit Cambridge Official Walking Tours | Bridge of Sighs" title="Visit Cambridge Official Walking Tours | Bridge of Sighs">
		</div>
	</div>
</div>

<div id="experts-container">
	<div id="experts-header"><h3>Hosted by award-winning guides</h3></div>
	<img class="iotg" src="/assets/images/ta.svg" alt="Rated 4.5 stars on average on Tripadvisor" title="Rated 4.5 stars on average on Tripadvisor">
	<img class="iotg" src="/assets/images/iotg.svg" alt="Institute of Tourist Guiding" title="Institute of tourist guiding">
	<img class="iotg" src="/assets/images/iotg.svg" alt="Institute of tourist guiding" title="Institute of tourist guiding">	
</div>

<div id="next-up-container">
	<div id="next-up-header"><h2>Essential Cambridge<span class="primary-color">.</span></h2></div>
	<div id="next-up">
		<img id="avid" class="profile-image" src="/assets/images/avid-larizadeh-duggan.jpg" alt="Avid Larizadeh Duggan" title="Avid Larizadeh Duggan">
		<div class="profile">
			<p class="date">20th August 2020</p>
			<p class="name">Avid Larizadeh Duggan OBE, Entrepreneur and Investor</p>
			<p class="description">Avid is the ex-COO of <a href="https://www.kobaltmusic.com/?utm_source=productsurgery&utm_medium=website&utm_campaign=none" target="_blank">Kobalt</a>—the music services unicorn. She has been a General Partner at Google Ventures, an Associate at Accel, and a Product Manager at Skype and eBay. Her angel investments include Okta, which went public in 2017.</p>
		</div>
	</div>
</div>

<div id="quote-container">
	<div id="quotes-header"><h3>Feedback from guests</h3></div>
	<div id="quote-1" class="quote">
		<p>It was incredible value, and a safe space for feedback. I'd pay for this.</p>
	</div>
	<div id="quote-2" class="quote">
		<p>I found the session super useful. I'll keep you guys posted on progress.</p>
	</div>
	<div id="quote-3" class="quote">
		<p>We really enjoyed it, your feedback was very actionable.</p>
	</div>
</div>

<div class="explainer-container">
	<h2>Our guides<span class="secondary-color">.</span></h2>
	<p> Our community of Green and Blue Badge Guides love Cambridge and can’t wait to share it with you. They will tailor your experience to your needs and interests, and no two tours are the same. Green and Blue Badge Guides are accredited by the Institute of Tourist Guiding.</p>
</div>

<div class="explainer-container">
	<h2>Our city<span class="tertiary-color">.</span></h2>
	<p> You're a founder of an early-stage business that has a live product, and at least some initial usage. This quote by <a href="https://pmarchive.com/guide_to_startups_part4.html" target="_blank">Marc Andreessen</a> describes your current situation:</p>
	<div class="big-quote">
		<p>You can always feel when product-market fit is not happening. The customers aren't quite getting value out of the product, word of mouth isn't spreading, usage isn't growing that fast, press reviews are kind of ‘blah’, the sales cycle takes too long, and lots of deals never close.
		</p>
	</div>
	<div style="width:100%; height: 90px;"></div>
</div>

<script>
	document.addEventListener('DOMContentLoaded', function() {
	    var footer = document.getElementById('sticky-footer');
	    var button = document.getElementById('primary-button');
	    var buttonOffset = button.getBoundingClientRect();
	    var triggerHeight = window.pageYOffset + buttonOffset.top + buttonOffset.height*.6;
		window.onscroll = function() {
		    if (window.pageYOffset > triggerHeight) {
		        footer.classList.add("show-footer");
		    } else {
		        footer.classList.remove("show-footer");
		    }
		}
	}, false);

</script>