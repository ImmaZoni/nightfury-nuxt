<template>
  <v-container>
    <v-row>
      <v-app-bar app dark tile flex-row> 
            <v-col>
              <v-btn nuxt icon>
                <nuxt-link to="/">
                  <v-icon>
                    mdi-home
                  </v-icon>
                </nuxt-link>
              </v-btn>
            </v-col>
            <v-col>
              <v-btn nuxt text>
                <nuxt-link to="/Animals">Adopt & Foster</nuxt-link>
              </v-btn>
              <v-btn nuxt text>        
                <nuxt-link to="/Care&Rescue">Care & Rescue</nuxt-link>
              </v-btn>
              <v-btn nuxt text>        
                <nuxt-link to="/Sanctuary">Sanctuary</nuxt-link>    
              </v-btn>
              <v-btn nuxt text>      
                <nuxt-link to="/Donate">Donate</nuxt-link>         
              </v-btn>
              <v-btn nuxt text> 
                <nuxt-link to="/Blog">Blog</nuxt-link>
              </v-btn>
            </v-col>
            <v-col>
              <v-btn nuxt icon>
                <nuxt-link to="/">
                    <v-icon>
                      mdi-send
                    </v-icon>
                </nuxt-link>
              </v-btn>
              <v-btn nuxt icon>
                <nuxt-link to="/">
                    <v-icon>
                      mdi-facebook
                    </v-icon>
                </nuxt-link>
              </v-btn>
              <v-btn nuxt icon>
                <nuxt-link to="/">
                    <v-icon>
                      mdi-twitter
                    </v-icon>
                </nuxt-link>
              </v-btn>
              <v-btn nuxt icon>
                <nuxt-link to="/">
                    <v-icon>
                      mdi-instagram
                    </v-icon>
                </nuxt-link>
              </v-btn>
          </v-col>
      </v-app-bar>
    </v-row>
  </v-container>      
</template>
<style>

</style>
<script>
export default {
    
  }
</script>