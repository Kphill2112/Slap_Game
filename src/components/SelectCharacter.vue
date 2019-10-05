<template>
  <div class="container-fluid selectCharacter">
    <div class="row">
      <div class="col-lg-6 col-md-6">
        <h1 v-if="!gameInstance.currentPlayer">Select Below</h1>
        <h1 v-else>{{gameInstance.currentPlayer.ame}}</h1>
      </div>
      <div class="col-lg-6 col-md-6">
        <h1>Enemy Name</h1>
      </div>
    </div>


    <div class="row">
      <div class="col-lg-6 col-md-6 Portrait">

        <img v-if="!gameInstance.currentPlayer" src="https://pbs.twimg.com/media/CbDqppJUkAE2Q3S.jpg" alt="">
        <img v-else :src="gameInstance.currentPlayer.Image_URL" alt="">
        <div class="col-lg-12 col-md-12 Roster">
          <div v-for="character in gameInstance.characters" class="RosterSlot" @click="assignPlayer(character)">
            <img :src="character.Image_URL" alt="">
          </div>
        </div>
      </div>


      <div class="col-lg-6 col-md-6 Portrait">
        <img v-if="!gameInstance.currentEnemy" src="https://pbs.twimg.com/media/CbDqppJUkAE2Q3S.jpg" alt="">
        <img v-else :src="gameInstance.currentEnemy.Image_URL" alt="">
        <div class="col-lg-12 col-md-12 Roster">
          <div v-for="character in gameInstance.characters" class="RosterSlot" @click="assignEnemy(character)">
            <img :src="character.Image_URL" alt="">
          </div>
        </div>
      </div>
    </div>

    <fight :GI="gameInstance" />
  </div>
</template>

<script>
  import Fight from '../components/Fight.vue'

  export default {
    name: 'SelectCharacter',
    methods: {
      assignEnemy(character) {

        this.gameInstance.currentEnemy = character;
      },
      assignPlayer(character) {
        this.gameInstance.currentPlayer = character;
      }
    },
    components: {
      Fight
    },
    props: [''],
    data() {
      return {
        gameInstance: {
          currentEnemy: "",
          currentPlayer: "",


          characters: {
            Mario: {
              Name: "Mario",
              Image_URL: "http://www.pngmart.com/files/2/Mario-PNG-Image.png",
              Items: {
                Cape: {
                  Name: "Cape",
                  uses: -1,
                  attack: 0,
                  defense: 5,
                  health: 0,
                },
                Mushroom: {
                  Name: "Mushroom",
                  uses: 1,
                  attack: 0,
                  defense: 0,
                  health: 30,
                },
                FireFlower: {
                  Name: "FireFlower",
                  uses: 5,
                  attack: 10,
                  defense: 0,
                  health: 50,
                }
              },
              Attacks: {
                Slap: -3,
                Kick: -5,
                Punch: -10
              }
            },
            Bowser: {
              Name: "Bowser",
              Image_URL: "https://i.pinimg.com/originals/05/ea/ae/05eaaecd2ad77125570902fe1976dd2c.png",
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
  }


</script>

<style>
  .selectCharacter {
    height: auto;
    width: 95vw;
    background-color: rgba(0, 0, 0, 0.377);
    border: 2px solid black;
    margin: auto auto;
    object-fit: contain;
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
    cursor: pointer;
    max-height: 100px;
    max-width: auto;
    background-color: rgba(255, 255, 255, 0);
    border: 4px groove black;
    display: flex;
    justify-content: space-evenly;
    margin: auto auto;
    margin-bottom: 2vh;
    overflow: hidden;
  }

  .RosterSlot img {
    margin: -20px;
    max-height: 150px;
    max-width: 200px;
    min-height: 150px;
    min-width: 200px;
    object-fit: contain;
    overflow: hidden;
  }
</style>