<template>
    <v-app-bar app flat color="black">
      <v-container left>
        <nuxt-link to="/">
          <v-btn nuxt plain>
            <v-icon color="white" aria-hidden="false" x-large>
              mdi-home
            </v-icon>
          </v-btn>
        </nuxt-link>
        
        <nuxt-link to="/Animals">Adopt & Foster</nuxt-link>        
        <nuxt-link to="/Care&Rescue">Care & Rescue</nuxt-link>          
        <nuxt-link to="/Sanctuary">Sanctuary</nuxt-link>          
        <nuxt-link to="/Donate">Donate</nuxt-link>          
        <nuxt-link to="/Blog">Blog</nuxt-link>
      </v-container>
    </v-app-bar>
</template>
<script>
export default {
    
  }
</script>