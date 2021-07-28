<template>
  <v-card
    class="mx-auto"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="text-h5 mb-1">
          {{ mad.title }}
        </v-list-item-title>
        <v-list-item-subtitle>{{ mad.description }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-card-actions class="d-flex justify-center">
      <v-btn
        color="primary"
        nuxt
        :to="mad.url"
        style="text-decoration: none;"
      >
        Learn More About {{ mad.title }}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data () {
    return {
      mad: {
        title: 'Make A Difference!',
        description: 'Anyone Can Make A Difference!',
        profile: 'profile is here',
        url: '/make-a-difference'
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
