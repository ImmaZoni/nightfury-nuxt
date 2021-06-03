<template>
  <div>
    <v-menu
      attach="#navbar"
      transition="slide-y-transition"
      offset-y
      bottom
      eager
    >
      <template #activator="{ on, attrs }">
        <div>
          <v-btn v-bind="attrs" v-on="on">
            Our Sanctuary
          </v-btn>
        </div>
      </template>
      <v-list>
        <v-list-item to="/animals" nuxt>
          <v-list-item-title>
            Our Animals
          </v-list-item-title>
        </v-list-item>
        <v-list-item to="/about-us" nuxt>
          <v-list-item-title>
            About Us
          </v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
</script>
