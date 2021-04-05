<template>
  <v-app-bar>
    <v-row class="justify-center align-center" no-gutters>
            <v-col class="d-inline-flex justify-start">
              <v-btn nuxt icon>
                <nuxt-link to="/" style="text-decoration: none;">
                  <v-icon>
                    mdi-home
                  </v-icon>
                </nuxt-link>
              </v-btn>
            </v-col>
            <v-col class="d-inline-flex">
              <v-btn nuxt text >
                <nuxt-link to="/Animals" style="text-decoration: none;">Adopt & Foster</nuxt-link>
              </v-btn> 
              <v-btn nuxt text>        
                <nuxt-link to="/Care&Rescue" style="text-decoration: none;">Care & Rescue</nuxt-link>
              </v-btn>
              <v-btn nuxt text>        
                <nuxt-link to="/Sanctuary" style="text-decoration: none;">Sanctuary</nuxt-link>    
              </v-btn>
              <v-btn nuxt text>      
                <nuxt-link to="/Donate" style="text-decoration: none;">Donate</nuxt-link>         
              </v-btn>
              <v-btn nuxt text> 
                <nuxt-link to="/Blog" style="text-decoration: none;">Blog</nuxt-link>
              </v-btn>
            </v-col>
            <v-col class="d-inline-flex justify-end">
              <v-btn nuxt icon href="mailto:admin@thecircleoflifesanctuary.org" target="_blank">
                    <v-icon>
                      mdi-send
                    </v-icon>
              </v-btn>
              <v-btn nuxt icon href="https://www.facebook.com" target="_blank">
                    <v-icon>
                      mdi-facebook
                    </v-icon>
              </v-btn>
              <v-btn nuxt icon href="https://www.twitter.com" target="_blank">
                    <v-icon>
                      mdi-twitter
                    </v-icon>
              </v-btn>
              <v-btn nuxt icon href="https://www.instagram.com" target="_blank">
                    <v-icon>
                      mdi-instagram
                    </v-icon>
              </v-btn>
          </v-col>
    </v-row>
    
  </v-app-bar>      
</template>
<style>

</style>
<script>
export default {
    
  }
</script>