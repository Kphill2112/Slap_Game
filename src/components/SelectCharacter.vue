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
      <div class="col-lg-6 col-md-6 Portrait">
        <img :src="this.characters.Mario.Image_URL" alt="">
        <div class="col-lg-12 col-md-12 Roster">
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
        </div>
      </div>
      <div class="col-lg-6 col-md-6 Portrait">
        <img :src="this.characters.Bowser.Image_URL" alt="">
        <div class="col-lg-12 col-md-12 Roster">
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
          <div class="RosterSlot">

          </div>
        </div>
      </div>
    </div>
    <div class="row">

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
        enemyHover: "characters.Bowser",
        playerHover: "characters.Mario",

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
          },
          Bowser: {
            Name: "Bowser",
            Image_URL: "https://www.ssbwiki.com/images/thumb/4/49/Bowser_SSBU.png/1200px-Bowser_SSBU.png",
            Items: {
              Tough_Guy: "Tough Guy",
              Giga_Bowser: "Giga Bowser",
              Koopa_Car: "Koopa_Car",
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
    width: 95vw;
    background-color: rgba(0, 0, 0, 0.377);
    border: 2px solid black;
    margin: auto auto;
  }

  .Portrait img {
    max-height: 35vh;
    max-width: 35vw;
    margin-bottom: 3vh;
  }

  .Roster {
    display: flex;
  }

  .RosterSlot {
    max-height: 75px;
    max-width: 75px;
    min-height: 75px;
    min-width: 75px;

    background-color: white;
    border: 2px groove black;

    display: flex;
    justify-content: space-evenly;
    margin: auto auto;
    margin-bottom: 2vh;
  }
</style>