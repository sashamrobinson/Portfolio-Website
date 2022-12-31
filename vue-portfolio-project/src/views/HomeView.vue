<template>
  <div class="container">
    <!-- <Header /> -->
    <div id="bg">
      <Header />
    </div>
  </div>
</template>

<script>
import Header from '../components/Header'

export default {
  name: 'HomeView',
  components: {
    Header
  }
}
</script>

<style>
body, html {
  height: 100%;
  margin: 0;
}

#bg {
  /* The image used */
  background-image: url("../assets/biblical_painting_background.png");
  position: absolute;

  /* Full height */
  height: 100%;
  top: 0;
  left: 0;
  right: 0;

  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

</style>