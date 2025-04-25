<template>
  <section id="socialMedia" class="grid--c6">
    <div class="address">
      <ul>
        <li class="name">CraftedWild</li>
        <li>1021 Butterfield Rd.</li>
        <li>Vernon Hills, IL</li>
        <li>60061</li>

        <li class="number">(815) 290.WILD</li>
        <li class="social"><a href="mailto:info@craftedwild.com">info@craftedwild.com</a></li>
      </ul>
    </div>

    <div class="social">
      <ul class="fa-ul">
        <li><a href="https://www.houzz.com/pro/craftedwild/craftedwild-cabinetry" target="_blank"><span class="fa-li"><i class="fab fa-houzz"></i></span> Houzz</a></li>

        <li><a href="https://www.instagram.com/craftedwild/" target="_blank"><span class="fa-li"><i class="fab fa-instagram"></i></span> Instagram</a></li>

        <li><a href="https://www.facebook.com/CraftedWild" target="_blank"><span class="fa-li"><i class="fab fa-facebook"></i></span> Facebook</a></li>

        <li><a href="https://www.pinterest.com/craftedwild/modern-european-kitchens/" target="_blank"><span class="fa-li"><i class="fab fa-pinterest"></i></span> Pinterest</a></li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SocialMedia',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#socialMedia {
  height: 30vh;
  padding: 2.5em 1em 1em;
  color: #fff;
  background-color: #000;
  /* background-color: rgb(58,58,60); */
  line-height: 1.4;
  display: flex;
    flex-flow: row nowrap;
    justify-content: space-around;
}

li {
  list-style-type: none;
  text-align: left;
}

.address li {
  color: rgba(255,255,255,0.75);
}

.address .name {
  color: #fff;
  font-weight: bold;
}

.address .number {
  margin-top: 1em;
}

.social ul {
  padding-left: 0;
}

.social li {
  line-height: 2;
}

.social a {
  border-bottom: 1px solid rgba(255,255,255,0.50);
  color: rgba(255,255,255,0.75);
  transition: 0.75s;
}

.social a:focus,
.social a:hover {
  border-bottom: 1px solid rgba(255,255,255,1);
  color: rgb(226,0,26);
}

@media (max-width: 700px) {
  .grid--c6 {
    grid-column: span 12;
  }

  .address ul {
    padding: 0;
  }
}
</style>
