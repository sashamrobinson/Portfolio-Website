<template>
  <div id="container">
    <div class="bg-painting">
      <Header />
      <Intro />
    </div>
    <div class="bg-solid">

    </div>
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
  mounted() {
    window.addEventListener('scroll', () => {
      var scrollPos = window.scrollY;
      var imageHeight = this.$el.querySelector('.bg-solid').clientHeight
      var fadeEnd = imageHeight + imageHeight / 2

      if (scrollPos > fadeEnd) {
        this.$el.querySelector('bg-solid').style.opacity = 0
      }
      else {
        var opacity = 1 - scrollPos / fadeEnd
        this.$el.querySelector('bg-solid').style.opacity = opacity
      }
    })
  },
  methods: {

  }
}

</script>

<style>
#container {
  overflow-y: hidden;
}

.bg-painting {
  background-image: url("../assets/renaissance_painting.jpeg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: absolute;
  height: 125%;
  top: 0;
  left: 0;
  right: 0;

}
.bg-solid {
  background-color: black;
  position: relative;
  height: 100px;
  width: 100px;
  top: 10em;
  left: 0;
  right: 0;
  
}
</style>