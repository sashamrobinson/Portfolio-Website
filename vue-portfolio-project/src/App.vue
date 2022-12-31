<template id="scroll">
  <div class="container">
    <router-view id="test"/>
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
  }
}
</script>

<style>
#scroll {
  overflow-y: hidden;
  overflow-x: hidden;
  max-width: 100%;
  max-height: 100%; 
}
.container {
  overflow-y: scroll;
}
</style>
