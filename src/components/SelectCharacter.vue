<template>
  <div class="container-fluid selectCharacter">
    <div class="row">
      <div class="col-lg-6 col-md-6">
        <h1>Character Name</h1>
      </div>
      <div class="col-lg-6 col-md-6">
        <h1>Enemy Name</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-6 col-md-6 playerPortrait">
        <img :src="this.characters.Mario.Image_URL" alt="">
      </div>
      <div class="col-lg-6 col-md-6">
        <img src="" alt="">
      </div>
    </div>
    <div class="row">
      <div class="col-lg-12 col-md-12">

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'SelectCharacter',
    components: {

    },
    data() {
      return {
        enemyHover: "",
        playerHover: "",

        currentEnemy: "",
        currentPlayer: "",

        characters: {
          Mario: {
            Name: "Mario",
            Image_URL: "http://www.pngmart.com/files/2/Mario-PNG-Image.png",
            Items: {
              Cape: "Cape",
              Fire_Flower: "Fire Flower",
              Mushroom: "Mushroom",
            },
            Attacks: {
              Slap: -3,
              Kick: -5,
              Punch: -10
            }
          }
        }
      }
    }
  }


</script>

<style>
  .selectCharacter {
    height: auto;
    width: 80vw;
    background-color: rgba(0, 0, 0, 0.377);
    border: 2px solid black;
  }

  .playerPortrait img {
    max-height: 25vh;
    max-width: 25vw;
  }
</style>