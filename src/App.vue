<template>
  <div id="app">
    <the-header/>
    <the-footer/>
    <home/>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
import Home from './views/Home.vue'

export default {
  name: 'app',
  components: {
    TheHeader,
    TheFooter,
    Home
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
  #app {
    width: 80%;
    margin: 15px auto;
  }
}

@media (min-width: 1024px) {
  // desktop
  #app {
    width: 1000px;
    margin: 20px auto;
  }
}
</style>
