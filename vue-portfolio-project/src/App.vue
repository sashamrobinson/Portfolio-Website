<template id="scroll">
  <div>
    <router-view id="test" @click.native="$scrollToTop"/>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },
  data() {
    return {

    }
  },
  beforeCreate() {
    history.scrollRestoration = 'manual'
    window.scrollTo(0,0)
  }
}
</script>

<style>
body {
  overscroll-behavior-y: none;
  padding: 0;
  margin: 0;
  
}
.container {
  overflow-y: scroll;
}
@font-face {
    font-family: Tusker Grotesk;
    font-weight: 4500 Medium;
    src: url("./assets/TuskerGrotesk-4500Medium.ttf");
}
@font-face {
    font-family: Helvetica Now Display;
    font-weight: Thin;
    src: url('./assets/HelveticaNowDisplay-Thin.ttf');
}

</style>
