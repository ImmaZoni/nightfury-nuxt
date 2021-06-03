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
            Make A Difference
          </v-btn>
        </div>
      </template>
      <v-list>
        <v-list-item to="/adopt" nuxt>
          <v-list-item-title>
            Adopt
          </v-list-item-title>
        </v-list-item>
        <v-list-item to="/foster" nuxt>
          <v-list-item-title>
            Foster
          </v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
</script>
