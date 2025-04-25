<template>
  <section id="map" class="grid--c6">
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5907.24671794497!2d-87.9770465!3d42.2438589!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x880f97b3e50d3b8f%3A0xd66b9e0aea009d44!2s1021%20Butterfield%20Rd%2C%20Vernon%20Hills%2C%20IL%2060061!5e0!3m2!1sen!2sus!4v1745599477199!5m2!1sen!2sus" width="80%" height="80%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
	
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
