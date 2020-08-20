<template>
  <v-app>
    <v-app-bar      
      dark
      app
    >      
    </v-app-bar>
      <Header />
    <v-main>
      <Body />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Body from './components/Body.vue'


export default {
  name: 'App',

  components: {
    Header,
    Footer,
    Body,
  },

  data: () => ({
    //
  }),
};
</script>
