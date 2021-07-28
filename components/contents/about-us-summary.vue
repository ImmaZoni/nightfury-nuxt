<template>
  <v-card
    align="center"
    class="mx-auto pa-5"
    color="backgroundsecondary"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="text-h2">
          {{ about.title }}
        </v-list-item-title>
        <v-list-item-subtitle class="d-flex text-h5">
          {{ about.description }}
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-card-actions class="d-flex justify-center">
      <v-btn
        color="primary"
        nuxt
        :to="about.url"
        style="text-decoration: none;"
      >
        Learn More About {{ about.title }}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data () {
    return {
      about: {
        title: 'About Us',
        description: 'We are an up and coming animal sanctuary based in Phoenix, Arizona striving to help all the animals we can. We are currently working with a limited capacity, but will continue to help every animal in any way possible. We will update our website with the progression of our non profit. For all inquiries and questions you may contact us at anytime at Admin@thecircleoflifesanctuary.org Please stay tuned for more updates, thank you for all your donations and support!',
        url: '/about-us'
      }
    }
  }
}
</script>
