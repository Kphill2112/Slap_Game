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
    font-family: 'Press Start 2P', cursive;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /* background: url('./assets/ben-neale-zpxKdH_xNSI-unsplash.jpg') no-repeat center center fixed; */
    background-size: cover;
    position: fixed;
    min-height: 100%;
    width: 100vw;
    height: auto;
    top: 0;
    left: 0;
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