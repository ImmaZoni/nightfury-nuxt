<template>
  <div>
    <v-toolbar>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>
        The Circle of Life Animal Santuary
      </v-toolbar-title>
    </v-toolbar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-app-bar>
        <v-icon @click.stop="drawer = !drawer">
          mdi-close
        </v-icon>
      </v-app-bar>
      <v-list>
        <v-list-item nuxt to="/">
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-group
          v-for="nav in navs"
          :key="nav.title"
          v-model="nav.active"
          :prepend-icon="nav.icon"
          no-icon
        >
          <template #activator>
            <v-list-item-content>
              <v-list-item-title v-text="nav.title" />
            </v-list-item-content>
          </template>

          <v-list-item
            v-for="child in nav.items"
            :key="child.title"
            nuxt
            :to="child.to"
          >
            <v-list-item-content>
              <v-list-item-title v-text="child.title" />
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          v-model="item.active"
          :prepend-icon="item.icon"
          nuxt
          :to="item.to"
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
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
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
    navs: [
      {
        icon: '',
        items: [
          { title: 'Adopt', to: '/adopt' },
          { title: 'Foster', to: '/foster' },
          { title: 'Donate', to: '/donate' }
        ],
        title: 'Make A Difference'
      },
      {
        icon: '',
        items: [
          { title: 'Resources', to: '/resources' },
          { title: 'Animal Information', to: '/animal-information' }
        ],
        title: 'Care & Rescue'
      },
      {
        icon: '',
        items: [
          { title: 'Our Animals', to: '/our-animals' },
          { title: 'About Us', to: '/about-us' }
        ],
        title: 'Our Sanctuary'
      }
    ],
    items: [
      {
        icon: '',
        title: 'Blog',
        to: '/blog'
      }]
  }),
  watch: {
    group () {
      this.drawer = false
    }
  }
}
</script>
