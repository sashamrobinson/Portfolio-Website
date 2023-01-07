<template>
  <div class="bg-solid">
    <div class="bg" id="image" :style="{ opacity: backgroundOpacity}"></div>
    <Header />
    <Intro id="intro"/>
    <AboutMe id="about"/>
    <Projects />
    <div></div>
  </div>
</template>

<script>
import Header from '../components/Header'
import Intro from '../components/Intro'
import AboutMe from '../components/AboutMe'
import Projects from '../components/Projects'

export default {
  name: 'HomeView',
  components: {
    Header,
    Intro,
    AboutMe,
    Projects
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
    this.animateTitle()
  },
  methods: {
    animateTitle() {
      // TODO
    },
    fadeOnScroll() {
      window.addEventListener('scroll', () => {
        const checkPoint = 900;
        let scrollPos = window.scrollY;
        let opacity;
        if (scrollPos <= checkPoint) {
          opacity = 0.4 - scrollPos / checkPoint 
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
        if (currentOpacity <= 0.4) {

          clearInterval(fadeInterval)
        }
      }, 50)
    }
  }
}

</script>

<style>
#intro {
  animation-name: slide-animation;
  animation-duration: 2s;
}
@keyframes slide-animation {
  from {
    transform: translateX(-40em)
  }
  to {
      transform: translateX(0em);
  }
}
#about {
  animation-name: slide-animation-reverse;
  animation-duration: 2s;
}

@keyframes slide-animation-reverse {
  from {
    transform: translateX(50em)
  }
  to {
    transform: translateX(0em)
  }
}
.bg {
  background-image: url("../assets/test.jpeg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: absolute;
  height: 150%;
  top: 0;
  left: 0;
  right: 0;
}
.bg-solid {
  background-color: #868b8b;
  height: 150em;
  width: 100%;
  
}
.sub-title {
    font-family: Helvetica Now Display;
    letter-spacing: 0.5em;
    color: white;
    font-size: 1.2em;
}
.sub-title-2 {
    font-family: "Tahoma";
    font-style: normal;
    font-weight: 700;
    font-size: 1em;
    letter-spacing: 0.045em;
    color: white;
    margin-right: 1em;
    text-shadow: 0px 4px 4px
        rgba(0, 0, 0, 0.25)
}

</style>