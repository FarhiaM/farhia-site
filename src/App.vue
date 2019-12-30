<template>
  <div id="app">
    <Main/>
    <Contact/>
  </div>
</template>

<script>
import Main from './components/Main.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'app',
  components: {
    Main,
    Contact
    }
}
</script>

<style lang="scss">
body {
  margin:0; /* This is used to reset any browser-default margins */ 
  }


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin:0;
}

@media (min-width: 768px) and (max-width: 1023px) {
  // tablet
  #app {
    width: 80%;
  }
}

@media (min-width: 1024px) {
  // desktop
  #app {
  }
}
</style>
