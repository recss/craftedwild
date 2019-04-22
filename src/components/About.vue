<template>
  <section id="about" class="grid--c12">
    <h2>About Us</h2>

    <div style="width: 80vw; margin: 0 auto;">
    	<img src="https://res.cloudinary.com/craftedwild/image/upload/c_scale,w_900/v1555946205/barrington__modern-gem/pdetphotography-craftedwild-280-leeds-barrington_5.jpg" style="border: 2px solid #fff;">
    </div>

    <div class="profile-img-full">
    	<div class="profile-img-full__kip"><strong>Kyle</strong> brings over a decade worth of operations, sales and customer experience to the table and leads business operations at CraftedWild. As a newcomer to the cabinetry and remodeling industries, he understood that the high quality product is a table stake. The white-glove, catered experience delivered to each client, however, is what makes CraftedWild standout.</div>

    	<div class="profile-img-full__kornel"><strong>Kornel</strong> is a third-generation wood craftsman, and leads CraftedWild’s production operations. From creating a design based on client’s vision, to the entire manufacturing process from planning, to first cut, to installation and inspection – Kornel applies highest level of quality during every step.</div>
    </div>

	<!-- <div class="profile kip">
		<div class="profile-pic"></div>
		<p><strong>Kyle</strong> brings over a decade worth of operations, sales and customer experience to the table and leads business operations at CraftedWild. As a newcomer to the cabinetry and remodeling industries, he understood that the high quality product is a table stake. The white-glove, catered experience delivered to each client, however, is what makes CraftedWild standout.</p>
	</div>

	<div class="profile kornel">
		<p><strong>Kornel</strong> is a third-generation wood craftsman, and leads CraftedWild’s production operations. From creating a design based on client’s vision, to the entire manufacturing process from planning, to first cut, to installation and inspection – Kornel applies highest level of quality during every step.</p>
		<div class="profile-pic"></div>
	</div> -->

	<!--  -->

	<!-- <div class="profile-text">
		<p>By passionately delivering both the personalized experience our clients deserve and innovative high-quality products they want, we are challenging the cabinetry status quo.  We promise to keep you informed and in-control throughout the process, while making sure you are THRILLED with the result.</p>

		<p>We are CraftedWild, a full-service cabinetry shop specializing in the design, manufacturing and installation of high-end modern and contemporary kitchens, closets and more.</p>
	</div> -->
  </section>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#about {
	padding: 1em;
	color: #fff;
	background-color: #000;
	/* background-color: rgb(58,58,60); */
	line-height: 1.4;
}

.profile {
	width: 70vw;
	margin: 0 auto;
	padding-bottom: 1.5em;
	display: flex;
		flex-flow: row nowrap;
		justify-content: center;
		align-items: flex-start;
}

.profile p,
.profile-text p {
	max-width: 40em;
}

.profile-img-full {
	width: 80vw;
	margin: 0 auto;
	display: flex;
	flex-flow: row nowrap;
	flex: 0 0 auto;
	justify-content: center;
}

.profile-img-full__kip,
.profile-img-full__kornel {
	flex-basis: 50%;
	padding: 2em;
	text-align: left;
}

.profile-pic {
	height: 10em;
	flex: 0 0 10em;
	border: 1px solid #fff;
	border-radius: 10em;
	/*box-shadow: 0px 0px 10px 2.5px rgba(255,255,255,0.75);*/
	background-size: cover;
}

.kip p {
	text-align: left;
}

.kip .profile-pic {
	margin-right: 2em;
	background-image: url("https://res.cloudinary.com/craftedwild/image/upload/v1555947543/CraftedWild_team/kip--barrington.jpg");
	background-position: center;
	/*transform: rotate(5deg);*/
}

.kornel p {
	text-align: right;
}

.kornel .profile-pic {
	margin-left: 2em;
	background-image: url("https://res.cloudinary.com/craftedwild/image/upload/v1555947543/CraftedWild_team/kornel--barrington.jpg");
	background-position: -6px top;
	/*transform: rotate(-3deg);*/
}

.profile-text {
	width: 70vw;
	margin: 1.25em auto 0;
	border-top: 1px solid rgba(255,255,255,0.15);
	padding-top: 1.5em;
	padding-bottom: 1.5em;
	text-align: left;
	display: flex;
		flex-flow: column nowrap;
		justify-content: center;
		align-items: center;
}

@media (max-width: 700px) {
	.profile {
		flex-flow: column nowrap;
		align-items: center;
	}

	.profile,
	.profile-text {
		width: 80vw;
	}

	.profile-img-full {
		flex-flow: column nowrap;
	}

	.profile-img-full__kip {
		flex-basis: 100%;
		padding: 2em 2em 1em;
	}

	.profile-img-full__kornel {
		flex-basis: 100%;
		padding: 1em 2em 2em;
	}

	.profile-pic {
		width: 10em;
	}

	.profile p {
		padding-top: 1em;
		text-align: left;
	}

	.kornel .profile-pic {
		order: 0;
	}

	.kornel p:first-of-type {
		order: 1;
	}

	.kip .profile-pic,
	.kornel .profile-pic {
		margin: 0;
	}
}
</style>
