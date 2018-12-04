<template>
  <section id="testimonials" class="grid--c12">
	<!-- <div class="quotes">
		<p>&ldquo;</p>
	</div> -->

	<!-- <div class="review">
		<p>Many thanks to Kornel and Kyle of CraftedWild Cabinetry for generating the very best quality kitchen for a complete rehab home project. These two have been truly a pleasure to work with. They give great attention to your detailed needs, then produce the perfect product just as you envisioned it! This catered approach, and their timeliness are gems in this industry. They truly care for their clients and put forth their best efforts to ensure that you are 100% happy and satisfied with the end result. CraftedWild is amazing in every aspect, everything from consultation to the finished product has been such an easy, hassle-free process, that repeat business is a no-brainer. They are no doubt always our first choice in custom cabinetry in the whole Chicagoland area.</p>
		<p class="reviewer">&mdash; Shiella C.</p>
	</div> -->

	<!-- <div class="review">
		<p>Kyle, Kornel, and the whole CraftedWild Team we’re amazing through every step of our whole home remodel. They helped us create my dream modern kitchen, two bathrooms vanities, and a laundry room nook. They were very patient and helpful throughout the entire design process, making every modification and request that I needed to help settle on my perfect plan. Their craftsmanship ability and attention to detail is impressive. They also make you feel like you’re their only client. Very nice work, guys.</p>
		<p class="reviewer">&mdash; Leigh B.</p>
	</div> -->

	<div class="review">
		<p>CraftedWild are among the very best millworkers I’ve encountered. The level of craftmanship in their fabrication is outstanding, and their installations are undertaken with great care and precision. Throughout the design and construction process they are fully engaged, timely and responsive. Kyle and Kornel are a pleasure to work with, and bring a depth of knowledge and expertise to all aspects of their projects. The quality of their work is a result of both their skill as millworkers, but also the high-level of service and thoughtfulness they provide throughout the process.</p>
		<p class="reviewer">&mdash; Eric R.</p>
		
		<p style="text-align: center;"><a href="https://www.houzz.com/pro/craftedwild/craftedwild-cabinetry" target="_blank">Read more reviews on Houzz</a></p>
	</div>

	<!-- <div class="quotes">
		<p>&rdquo;</p>
	</div> -->
  </section>
</template>

<script>
export default {
  name: 'Testimonials',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#testimonials {
	padding: 1em;
	color: #fff;
	background-color: #0f0f0f;
	/* background-color: rgb(58,58,60); */
	line-height: 1.4;
	display: flex;
		justify-content: center;
}

.quotes {
	font-size: 4em;
}

.quotes p {
	margin: 0;
}

.review {
	height: 100%;
	width: 50vw;
	text-align: left;
	display: flex;
		flex-flow: column nowrap;
		justify-content: center;
}

.review p:first-child {
	border-left: 0.25em solid #fff;
	padding: 0.25em 0 0.25em 1em;
	color: rgba(255,255,255,0.75);
	line-height: 1.5;
}

.reviewer {
	text-align: right;
	font-weight: bold;
}

a {
  border-bottom: 1px solid rgba(255,255,255,0.50);
  color: rgba(255,255,255,0.75);
  transition: 0.75s;
}

a:focus,
a:hover {
  border-bottom: 1px solid rgba(255,255,255,1);
  color: rgb(226,0,26);
}

@media (max-width: 700px) {
	.review {
		width: 85vw;
	}
}
</style>
