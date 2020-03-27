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
    <div style="margin: 1em 0; grid-column: span 12; display: flex; justify-content: center; align-items: center;">
      <!--  -->
      <a href="http://www.homeadvisor.com/rated.CraftedWild.62195262.html" target="_blank" style="margin-right: 1em; display: block;">
        <img alt="CraftedWild is a HomeAdvisor Screened & Approved Pro" style="height: 6em; display: block;" src="http://www.homeadvisor.com/images/sp-badges/soap-solid-border.png?sp=62195262&key=9b0fd57a3144ed94bbc31aee01d88a6a">
      </a>

      <table style="width: 80px; margin-right: 1em;" cellpadding="0" cellspacing="0">
        <tr>
          <td>
            <a href="https://www.houzz.com/pro/craftedwild/craftedwild-cabinetry">
              <img src="https://st.hzcdn.com/static/badge_44_8@2x.png" alt="Kyle Kiperman in Elk Grove Village, IL on Houzz" width="80" height="80" border="0" />
            </a>
          </td>
        </tr>
      </table>

      <table style="width: 80px; margin-right: 1em;" cellpadding="0" cellspacing="0">
        <tr>
          <td>
            <a href="https://www.houzz.com/pro/craftedwild/craftedwild-cabinetry">
              <img src="https://st.hzcdn.com/static/badge_47_8@2x.png" alt="Kyle Kiperman in Elk Grove Village, IL on Houzz" width="80" height="80" border="0" />
            </a>
          </td>
        </tr>
      </table>

	  <table style="width: 80px;" cellpadding="0" cellspacing="0">
		  <tr>
			  <td>
					<a href="https://www.houzz.com/pro/craftedwild/craftedwild-cabinetry">
				  	<img src="https://st.hzcdn.com/static/badge_49_8@2x.png" alt="Kornel Tadeuszuk in Elk Grove Village, IL on Houzz" width="80" height="80" border="0" />
					</a>
				</td>
			</tr>
		</table>
      <!--  -->
    </div>
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
