<template>
  <v-card
    class="mx-auto"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="text-overline mb-4">
          ANIMAL SPOTLIGHT
        </div>
        <v-list-item-title class="text-h5 mb-1">
          {{ animal.name }}
        </v-list-item-title>
        <v-list-item-subtitle>{{ animal.description }}</v-list-item-subtitle>
      </v-list-item-content>
      <v-list-item-avatar
        color="grey"
      >
        <v-img :src="TempProfile" />
      </v-list-item-avatar>
    </v-list-item>

    <v-card-actions class="d-flex justify-center">
      <v-btn
        color="primary"
        nuxt
        :to="animal.url"
        style="text-decoration: none;"
      >
        Learn More About {{ animal.name }}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data () {
    return {
      animal: {
        name: 'Athena',
        description: 'Athena is our kitty!',
        profile: 'profile is here',
        url: '/animals/athena'
      }
    }
  },
  computed: {
    TempProfile () {
      return 'TempProfile.jpg'
    }
  }
}
</script>
