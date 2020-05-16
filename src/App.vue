<template>
  <div id="app">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
    <Main/>
  </div>
</template>

<script>
import Main from './components/Main.vue'

export default {
  name: 'app',
  components: {
    Main
    }
}
</script>

<style lang="scss">
body {
  margin:0; 
  background-color: #151D26;
  font-family: Arial;
  }

@media screen and (prefers-color-scheme: light) {
  body {
    background-color: white;
  }
}


#app {
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
