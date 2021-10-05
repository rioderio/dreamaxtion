<template>
  <div id="app">
    <newApp />
  </div>
</template>

<script>
import newApp from './components/newApp.vue'

export default {
  name: 'App',
  components: {
    newApp
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
