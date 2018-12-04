<template>
  <div id="app" class="grid">
    <Navigation @clicked="inputContactClick" />
    <section id="navigation-placeholder"></section>
    <Hero/>

    <About/>
    <Process/>
    <Projects/>

    <Testimonials/>
    <SocialMedia/>
    <Map/>
    <Contact v-if="showContact()" />
  </div>
</template>

<script>
import Navigation from './components/Navigation'
import Hero from './components/Hero'
import About from './components/About'
import Process from './components/Process'
import Projects from './components/Projects'
import Testimonials from './components/Testimonials'
import SocialMedia from './components/SocialMedia'
import Map from './components/Map'
import Contact from './components/Contact'

export default {
  name: 'App',
  components: {
    Navigation, Hero, About, Process, Projects, Testimonials, SocialMedia, Map, Contact
  },
  data () {
    return {
      inputContact: false
    }
  },
  methods: {
    inputContactClick(value) {
      this.inputContact = value;
    },
    showContact() {
      if(document.documentElement.clientWidth <= 700 || this.inputContact) {
        return true;
      }
    }
  }
}
</script>

<style>
*,
*:before,
*:after {
    box-sizing: border-box;
}

html,
body {
    height: 100%;
    margin: 0;
    padding: 0;
    background-color: #000;
    -webkit-font-smoothing: antialiased;
    -moz-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-rendering: optimizelegibility;
}

a {
  text-decoration: none;
}

img {
  max-width: 100%;
}

h2 {
  margin: 1em 0 1.5em;
  border-bottom: 1px solid #fff;
  display: inline-block;
}

#app {
  font-family: 'Poppins';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: center;
}

.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows:
    5em
    70vh
    minmax(20vh, auto)
    minmax(20vh, auto)

    minmax(40vh, auto)

    minmax(20vh, auto)
    minmax(30vh, auto);
  /* navigation, hero, about, process, projects, testimonials, footer */
  grid-column-gap: 0;
}

.grid--c12 {
  grid-column: span 12;
}

.grid--c6 {
  grid-column: span 6;
}

.grid--c4 {
  grid-column: span 4;
}

.grid--c3 {
  grid-column: span 3;
}

@media (max-width: 700px) {
  .grid {
    grid-template-rows:
      5em
      70vh
      minmax(20vh, auto)
      minmax(20vh, auto)

      minmax(40vh, auto)

      minmax(20vh, auto)
      minmax(30vh, auto)
      minmax(30vh, auto);
    /* navigation, hero, about, process, projects, testimonials, footer */
    grid-column-gap: 0;
  }
}
</style>
