<template>
  <div class="wrap"></div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <HelloWorld1 msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HelloWorld1 from './components/HelloWorld1.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    HelloWorld1
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #d3e0ed;
  
}
.wrap{
  background-color: #181717;

}
</style>
