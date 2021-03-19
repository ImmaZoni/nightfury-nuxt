<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="flex green white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Help us Make a Difference!
      </v-card-text>
      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Circle of Life Animal Sanctuary</strong> - Phoenix, Arizona
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>