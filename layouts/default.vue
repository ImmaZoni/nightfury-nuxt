<template>
  <v-app>
    <Navigation2 />
      <v-main>
        <v-container>
          <nuxt />
        </v-container>
      </v-main>
    <div>
      <Footer />
    </div>
  </v-app>
</template>
<style>
a.nuxt-link-exact-active {
  font-weight: bold;
  color: #ffffff;
}
.router-link {
  display: inline-block;
  text-decoration: none;
}
</style>
<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
