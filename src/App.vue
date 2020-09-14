<template>
  <div id="app">
    <Appbar />
    <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
  </div>
</template>

<script>
import Appbar from './components/Appbar.vue'

export default {
  name: 'app',
  components: {
    Appbar,
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html {
  overflow: hidden;
}
</style>
