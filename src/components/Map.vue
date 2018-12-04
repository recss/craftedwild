<template>
  <section id="map" class="grid--c6">
	<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2963.635390124358!2d-87.985110784984!3d42.029553563902304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x880fa94bcd9cb4a1%3A0xd3ae91aa8a695a16!2sCraftedWild+Cabinetry!5e0!3m2!1sen!2sus!4v1507006626304" width="80%" height="80%" frameborder="0" style="border:0" allowfullscreen=""></iframe>
	
    <p>Showroom visits by appointment only.</p>
  </section>
</template>

<script>
export default {
  name: 'Map',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#map {
  height: 30vh;
	padding: 2.5em 1em 1em;
	color: #fff;
	background-color: #000;
	/* background-color: rgb(58,58,60); */
	line-height: 1.4;
}

@media (max-width: 700px) {
  #map {
    margin-bottom: 2em;
  }

  .grid--c6 {
    grid-column: span 12;
  }
}
</style>
