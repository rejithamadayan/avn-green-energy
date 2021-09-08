<template>
  <div id="app">
   <AvnHomePage/>
  </div>
</template>

<script>
import AvnHomePage from './components/avnHomePage.vue'
export default {
  name: 'App',
  components: {
    AvnHomePage
  }
}
</script>

<style>
html{
  overflow-x: hidden !important;
}
body {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
