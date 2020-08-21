<template>
    <div class='userProfile'>
        
        <v-icon @click="drawer = !drawer" size="100" class="teal darken-2"
        
        >mdi-gamepad-variant</v-icon>
        <v-navigation-drawer app class="grey darken-4" v-model="drawer">
        
<v-card
    class="mx-auto"
    max-width="600"
    tile
  >
 
   
      <v-row
        align="end"
        class="fill-height"
      >
        <v-col
          align-self="start"
          class="pa-0"
          cols="12"
        >
        <div class="row align-center justify-center">
          <div
            class="v-avatar grey darken-4 rounded-0"
            image = "true"
            style="height: 150px; min-width: 92px; width: 150px"
            
          >
          <img src="../assets/profileuser1.png" />
          </div>
          </div>
        </v-col>
        <v-col class="py-0">
          <v-list-item
            color="rgba(0, 0, 0, .4)"
            dark
          >
           <v-list-item-content class="teal--text">
              <v-list-item-title class="teal--text"><v-icon>mdi-github-box</v-icon>github.com/lucasdpassos</v-list-item-title>
              <v-list-item-subtitle class="teal--text"><v-icon>mdi-account</v-icon> Lucas Dezerto Passos</v-list-item-subtitle>
              <v-list-item-subtitle class="teal--text"><v-icon>mdi-gamepad</v-icon> Biblioteca de Jogos: 8</v-list-item-subtitle>
              <v-list-item-subtitle class="teal--text"><v-icon>mdi-clock</v-icon> Horas jogadas: 1338</v-list-item-subtitle>
            </v-list-item-content>
           </v-list-item>
           </v-col>
      </v-row>
    
</v-card>
        </v-navigation-drawer>
</div>

</template>

<script>



export default {
    data() {
        return {
        drawer: false,
    }}
}
</script>

<style scoped>
    .userProfile {
        margin: 0 auto;
        display: flex;
        justify-content: center;
        margin-top: 12%;
    }
</style>>