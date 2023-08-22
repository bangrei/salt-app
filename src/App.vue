<template>
  <HelloWorld/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
  html {
    height: 100%;
    width: 100%;
  }

  body {
    font-size: 100%;
    height: 100%;
    margin: 0;
    width: 100%;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
    height: 100%;
    width: 100%;
    overflow: hidden;
    overflow-y: auto;
  }
</style>
