<template>
<v-app>
  <v-app-bar dark>
      <Navigation-inprogress />
  </v-app-bar>  
      <v-main>
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
