<template>
  <div id="app">    
    <appHeader></appHeader>
    <Todos></Todos>
    <Footerer></Footerer>
    
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todo.vue'
import Footerer from './components/Footer.vue'
import appHeader from './components/Header.vue'

export default {
  name: 'app',
  components: {
    Todos,
    Footerer,
    appHeader,
    // HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
