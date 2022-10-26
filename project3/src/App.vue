<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <CompositionApi/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import CompositionApi from './components/CompositionApi.vue'

export default {
  name: 'App',
  components: {
    CompositionApi
    // HelloWorld
    ,
  
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
