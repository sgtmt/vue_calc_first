<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Calc />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Calc from './components/Calc'

export default {
  name: 'App',
  components: {
    Calc,
    HelloWorld
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
  margin-top: 60px;
}
</style>
