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
            Care & Rescue
          </v-btn>
        </div>
      </template>
      <v-list>
        <v-list-item to="/resources" nuxt>
          <v-list-item-title>
            Resources
          </v-list-item-title>
        </v-list-item>
        <v-list-item to="/information" nuxt>
          <v-list-item-title>
            Animal Information
          </v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
</script>
