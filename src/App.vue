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
			<a href="https://www.google.com/url?q=https://issuu.com/sandow-media/docs/ch_lx60_digital?e%3D6134964/77429769&sa=D&source=hangouts&ust=1596416839297000&usg=AFQjCNHqu4cTMu8CRI98YRZt5AQYSexRYg" target="_blank">
				<img src="https://res.cloudinary.com/craftedwild/image/upload/v1596330835/CraftedWild_acclaim/logo-luxe-white.png" alt="Luxe MagazineLuxe Interiors + Design">
			</a>

			<a href="https://www.google.com/url?q=https://chicago.curbed.com/2018/9/24/17885994/chicago-home-tour-mies-van-der-rohe-commonwealth-promenade&sa=D&source=hangouts&ust=1596416839297000&usg=AFQjCNF6RS51_6votxpfB6hDCtFqihBPFw" target="_blank">
				<img src="https://res.cloudinary.com/craftedwild/image/upload/v1596330835/CraftedWild_acclaim/curbed-chicago_logo.jpg" alt="Chicago Curbed">
			</a>

			<p><a href="https://www.journal-topics.com/pageview/viewer/EGBusinessJournal-2018-12-13#page=0" target="_blank">Elk Grove Business Journal</a></p>
			<!--  -->
    </div>

	<div style="margin-bottom: 1em; grid-column: 2/12; color: rgba(255,255,255,0.35); display: flex; justify-content: center; align-items: center;" class="signature">
		Made by &nbsp; <a href="https://www.re-css.com/" target="_blank">Kevin K. Johnson, II</a>.
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

.signature a {
  border-bottom: 1px solid rgba(255,255,255,0.5);
  color: rgba(255,255,255,0.35);
  transition: 0.75s;
}

.signature a:focus,
.signature a:hover {
  border-bottom: 1px solid rgba(255,255,255,0.75);
  color: rgb(226,0,26);
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
