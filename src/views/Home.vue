<template>
  <div class="home container-fluid">
    <div class="row">
      <div class="navbar col-lg-12 col-md-12">
        <div class="row homeLogo">
          <div class="col-lg-4 col-md-12 ">
            <p>Home</p>
          </div>
          <div class="col-lg-4 col-md-12 ">
            <p>Characters</p>
          </div>
          <div class="col-lg-4 col-md-12 ">
            <p>About</p>
          </div>
        </div>
      </div>
    </div>

    <selectCharacter />



  </div>
</template>

<script>
  import selectCharacter from '../components/SelectCharacter.vue'



  export default {
    data() {
      return {

      }
    },
    name: 'Home',
    components: {
      selectCharacter,
    }
  }



</script>

<style>
  .navbar {
    display: flex;
    margin: 1% auto;
    align-content: center;
    height: auto;
    width: 80vw;
    background-color: rgba(0, 0, 0, 0.377);
    border: 2px solid black;
    text-align: center;
  }

  .homeLogo {
    display: flex;
    text-align: center;
    width: 100vw;
    margin: auto auto;
  }

  .homeLogo p {

    cursor: pointer;
    vertical-align: middle;
    font-size: 1.5em;
    line-height: 2;
    text-align: center;


  }

  .homeLogo p:hover {
    -webkit-animation: flicker 1s linear infinite;

  }

  @-webkit-keyframes flicker {
    0% {
      opacity: 0;
      text-shadow: 2px 2px #f291ff;
    }

    9% {
      opacity: 0;
      text-shadow: 2px 2px #f291ff;
    }

    10% {
      opacity: .5;
      text-shadow: 2px 2px #f291ff;
    }
  }
</style>