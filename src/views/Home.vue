<template>
  <div class="home">
    <div class="navbar">
      <div class="homeLogo">
        <p>Home</p>
        <p>Characters</p>
        <p>About</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {

    }
  }


</script>

<style>
  .navbar {
    display: flex;
    margin-top: 5%;
    margin: 1% auto;
    align-content: center;
    height: 100px;
    width: 75%;
    background-color: gray;
    border: 2px solid black;
    text-align: center;
  }

  .homeLogo {
    display: table;
    text-align: center;
    width: 100%;
    overflow: hidden;
    padding: 1.5em .25em;

  }

  .homeLogo p {
    cursor: pointer;
    display: table-cell;
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
    }

    9% {
      opacity: 0;
    }

    10% {
      opacity: .5;
    }

    13% {
      opacity: 0;
    }
  }
</style>