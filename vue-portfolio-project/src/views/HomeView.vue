<template>
  <div class="bg-solid">
    <div class="bg" id="image" :style="{ opacity: backgroundOpacity}"></div>
      <Header />
      <Intro />
  </div>
</template>

<script>
import Header from '../components/Header'
import Intro from '../components/Intro'

export default {
  name: 'HomeView',
  components: {
    Header,
    Intro
  },
  data() {
    return {
      backgroundOpacity: 1,
    }
  },
  mounted() {
    document.getElementById('image').style.opacity = 0.5;
    this.fadeBackground()
    this.fadeOnScroll()
  },
  methods: {
    fadeOnScroll() {
      window.addEventListener('scroll', () => {
        const checkPoint = 900;
        let scrollPos = window.scrollY;
        let opacity;
        if (scrollPos <= checkPoint) {
          opacity = 0.35 - scrollPos / checkPoint 
        }

        else {
          opacity = 0
        }
        document.querySelector(".bg").style.opacity = opacity;
      })
    },
    fadeBackground() {
      const fadeDuration = 3000;
      const interval = fadeDuration / 50;
      const fadeIncrement = 1 / interval
      let currentOpacity = this.backgroundOpacity

      const fadeInterval = setInterval(() => {
        currentOpacity -= fadeIncrement
        this.backgroundOpacity = currentOpacity
        if (currentOpacity <= 0.35) {

          clearInterval(fadeInterval)
        }
      }, 50)
    }
  }
}

</script>

<style>
.bg {
  background-image: url("../assets/test.jpeg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: absolute;
  /*height: 125%;*/
  height: 150%;
  top: 0;
  left: 0;
  right: 0;
  /*transition: opacity 0.1s;*/
}
.bg-solid {
  background-color: #343232;
  height: 150em;
  width: 100%;
  
}

</style>