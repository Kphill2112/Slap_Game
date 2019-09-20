<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
  import Home from './views/Home.vue'


  //What did we learn?? 
  //To always export default, and name our components/views   = ´∇｀=
  //Components object too!
  export default {
    name: 'app',
    components: {
      Home
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
  }

  #nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }
</style>