<template>
    <div>
        <v-icon @click="drawer = !drawer" size="56" class="amber"
        
        >mdi-account</v-icon>
        <v-navigation-drawer app class="cyan" v-model="drawer">
<v-card
    class="mx-auto"
    max-width="434"
    tile
  >
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