<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/rogelio.jpeg" height="150" width="150">
    <Rogelio/>
    <footer>
      <p>¡Made with ❤️ en mi puta casa!</p>
    </footer>
  </div>
</template>

<script>
import Rogelio from './components/Rogelio.vue'

export default {
  name: 'App',
  components: {
    Rogelio
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
