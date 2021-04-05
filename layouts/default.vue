<template>
<v-app>
  <v-app-bar dark>
      <Navigation />
  </v-app-bar>  
      <v-main>
        <v-container>
          <Nuxt />
        </v-container>
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
