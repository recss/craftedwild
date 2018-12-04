<template>
  <section id="process" class="grid--c12">
    <h2>The Process</h2>

		<div class="profile-text">
			<p>By passionately delivering both the personalized experience our clients deserve and innovative high-quality products they want, we are challenging the cabinetry status quo.  We promise to keep you informed and in-control throughout the process, while making sure you are THRILLED with the result.</p>

			<p>We are CraftedWild, a full-service cabinetry shop specializing in the design, manufacturing and installation of high-end modern and contemporary kitchens, closets and more.</p>
		</div>

		<ul id="accordion">
			<li class="active">
				<div class="section-title">
					<h2>Consultation</h2>
				</div>
				<div class="section-content">
					<p>We measure the space and understand your vision, while answering any cabinetry questions you may have.</p>
				</div>
			</li>

			<li>
				<div class="section-title">
					<h2>Design</h2>
				</div>
				<div class="section-content">
					<p>A CraftedWild Designer recreates your vision as a rendering, giving you a visual representation of the finished product.</p>
				</div>
			</li>

			<li>
				<div class="section-title">
					<h2>Proposal</h2>
				</div>
				<div class="section-content">
					<p>Once you LOVE the design, we promptly deliver an official proposal.</p>
				</div>
			</li>

			<li>
				<div class="section-title">
					<h2>Production</h2>
				</div>
				<div class="section-content">
					<p>This is where the magic happens! Our team works to craft your dream cabinetry from scratch and keeps you updated throughout the buildout.</p>
				</div>    
			</li>

			<li>
				<div class="section-title">
					<h2>
						Delivery
						<br>+ Installation
					</h2>
				</div>
				<div class="section-content">
					<p>We carefully deliver your one-of-a-kind creation and get to work on installation.</p>
				</div>    
			</li>
		</ul>
  </section>
</template>

<script>
export default {
  name: 'Process',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#process {
	padding: 1em 1em 2em;
	color: #fff;
	background-color: #0f0f0f;
}

.profile-text {
	width: 70vw;
	margin: 0 auto;
	/* border-top: 1px solid rgba(255,255,255,0.15); */
	/* padding-top: 1.5em; */
	padding-bottom: 1.5em;
	text-align: left;
	display: flex;
		flex-flow: column nowrap;
		justify-content: center;
		align-items: center;
}

.profile-text p {
	max-width: 40em;
}

#accordion h2 {
	border: 0;
}

/* start: accordion */
/* https://codepen.io/anon/pen/odGQyq */

ul {
	display: flex;
	flex-flow: row nowrap;
  height: 50vh;
  margin: 0;
  padding: 0;
  overflow: hidden;
  list-style-type: none;
}

li {
  flex: 1;
  display: flex;
	align-items: stretch;
	border-left: 0.15em solid #000;
  padding: 20px;
  background: #0f0f0f;
  cursor: pointer;
	transition: all .5s ease;
}

li:first-of-type {
	border: 0;
}

li:focus,
li:hover {
	background: rgba(226,0,26,0.75);
	/* background: #62000B; */
}

li.active {
	flex: 5;
  background: rgb(226,0,26);
  cursor: default;
}

li.active h2 {
	color: #fff;
}

li.active .section-content {
	/* border-left: 1px solid #fff; */
	padding-left: 1.5em;
	display: flex;
	flex: 4;
  opacity: 1;
  transform: scaleX(1);
  color: #fff;
}

li .section-title {
	flex: 1;
	display: flex;
	align-items: center;
	width: 100%;
	margin: 0;
	padding: 0;
	text-align: center;
	color: #fff;
}

li .section-title h2 {
	margin: 0;
	transform: rotate(-90deg);
	white-space: nowrap;
}

li .section-content {
	flex: 1;
	display: none;
	align-items: center;
	margin: 0;
	padding: 0;
	opacity: 0;
	transition: all .25s .1s ease-out;
}

@media (max-width: 700px) {
	ul {
		height: auto;
	}

	.profile-text {
		width: 85vw;
	}
}

@media (max-width: 1200px) {
	ul {
		flex-flow: column nowrap;
	}

	li.active {
		flex: 100%;
	}

	li .section-title h2 {
		text-align: left;
		transform: rotate(0deg);
	}

	li.active .section-content {
		margin-left: 2em;
		border-left: 1px solid #fff;
	}
}

/* end: accordion */
</style>
