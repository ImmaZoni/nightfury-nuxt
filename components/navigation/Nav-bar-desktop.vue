<template>
  <v-app-bar fixed dark elevation="5">
    <v-row class="d-flex align-flex-auto">
      <v-col class="d-flex align-flex-auto">
        <v-btn nuxt icon>
          <nuxt-link to="/" style="text-decoration: none;">
            <v-icon>
              mdi-home
            </v-icon>
          </nuxt-link>
        </v-btn>
      </v-col>
      <v-spacer />
      <v-col class="d-inline-flex align-self-center justify-center">
        <div id="navbar" class="d-flex justify-space-between align-self-center">
          <make-a-difference-nav />
          <care-and-rescue-nav />
          <our-sanctuary-nav />
          <blog-nav />
        </div>
      </v-col>
      <v-spacer />
      <v-col class="d-inline-flex align-center justify-space-between justify-end">
        <v-btn nuxt icon href="mailto:admin@thecircleoflifesanctuary.org" target="_blank" small>
          <v-icon>
            mdi-send
          </v-icon>
        </v-btn>
        <v-btn nuxt icon href="https://www.facebook.com" target="_blank" small>
          <v-icon>
            mdi-facebook
          </v-icon>
        </v-btn>
        <v-btn nuxt icon href="https://www.twitter.com" target="_blank" small>
          <v-icon>
            mdi-twitter
          </v-icon>
        </v-btn>
        <v-btn nuxt icon href="https://www.instagram.com" target="_blank" small>
          <v-icon>
            mdi-instagram
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-app-bar>
</template>
<script>
export default {

}
</script>
<style>

</style>
