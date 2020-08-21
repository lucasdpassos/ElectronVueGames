<template>
    <v-app-bar        
    app
    dark     
    color='dark'   
    :src=logo
    style="width:300px;" 
    >
       
    </v-app-bar>
</template>


<script>



export default {
    data: () => {
     return {
        logo: require('../assets/electronvue.png')
    }}
}

</script>