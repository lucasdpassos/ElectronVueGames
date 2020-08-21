<template>
    <v-container>
    <v-row dense>       
        <v-col
          v-for="(game, i) in games"
          :key="i"
          cols="3"
        >
         <v-hover v-slot:default="{ hover }">
          <v-card            
            dark
            
          >
          <v-img
          :src="game.Bannersrc"
          >
          <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out teal darken-2 v-card--reveal display-1 white--text"
            style="height: 100%;"
             v-text="game.price"
          >
            
          </div>
        </v-expand-transition>
          
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="headline"
                  color='black'
                  v-text="game.title"
                ></v-card-title>

                <v-card-subtitle v-text="game.dev"></v-card-subtitle>
                
                
              </div>

             

              <v-avatar
                class="ma-3"
                size="140"
                tile
              >
                <v-img :src="game.cape"></v-img>
              </v-avatar>
            </div>
            </v-img>
          </v-card>
         </v-hover>
          
        </v-col>
      </v-row>
      <User />
    </v-container> 
    
</template>



<script>
import zelda from '../assets/zelda.jpg'
import eurotruck from '../assets/eurotruck.jpg'
import rocket from '../assets/rocket.jpg'
import sims4 from '../assets/sims4.jpg'
import ghost from '../assets/ghost.png'
import sonic from '../assets/sonic.jpg'
import goat from '../assets/goat.jpg'
import skyrim from '../assets/skyrim.jpg'
import User from './User'


export default {
    data: () => {
         return {
      current: {},
      index: 0,      
      games: [
        {
          cape: zelda,
          title: 'Legend of Zelda: Breath of the Wild',
          dev: 'Nintendo',
          Bannersrc: require('../assets/banners/zeldabanner.jpg'),
          price: "R$25,00"
        },
        {
          cape: eurotruck,
          title: 'Euro Truck Simulator',
          dev: 'SCS Software',
          Bannersrc: require('../assets/banners/eurotruckbanner.jpg'),
          price: "R$63,50"
        },
        {
          cape: sims4,
          title: 'The Sims 4',
          dev: 'EA',
          Bannersrc: require('../assets/banners/sims4banner.png'),
          price: "R$90,00"
        },
        {
          cape: rocket,
          title: 'Rocket League',
          dev: 'SCS Software',
          Bannersrc: require('../assets/banners/tocketbanner.jpg'),
          price: "R$25,00"
        },
        {
          cape: ghost,
          title: 'Ghost of Tsushima',
          dev: 'Sucker Punch Studio',
          Bannersrc: require('../assets/banners/ghostbanner.jpg'),
          price: "R$25,00"
        },
        {
          cape: goat,
          title: 'Goat Simulator',
          dev: 'Coffe Stain',
          Bannersrc: require('../assets/banners/goatbanner.jpg'),
          price: "R$20,00"
        },
        {
          cape: skyrim,
          title: 'The Elder Scrolls: V - Skyrim',
          dev: 'Bethesda',
          Bannersrc: require('../assets/banners/skyrimbanner.jpg'),
          price: "R$10,00"
        },
        {
          cape: sonic,
          title: 'Sonic Adventures',
          dev: 'SEGA',
          Bannersrc: require('../assets/banners/sonnicbanner.png'),
          price: "R$39,00"
        },     
                  
      ],
     
    }    
    },
    components: {
      User,
  },
    
}
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>