<template id="scroll">
  <div>
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
body {
  overscroll-behavior-y: none;
  padding: 0;
  margin: 0;
  
}

.container {
  overflow-y: scroll;
}

</style>
