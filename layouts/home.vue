<template>
<v-app> 
      <v-main>
        <Navigation />
        <Hero />
        <v-container></v-container>
        <Nuxt />
        <v-container></v-container>
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
