<template>
<v-app>
  <v-app-bar fixed dark>
      <Navigation />
  </v-app-bar>  
      <v-main>
        <v-img
            contain
            src="/Hero-Logo.svg"></v-img>
        <Nuxt />
        <v-spacer></v-spacer>
        <Footer />  
      </v-main>  
</v-app>
</template>


<style>

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
<script>
export default {
  data () {
    return {
    }
  }
}
</script>
