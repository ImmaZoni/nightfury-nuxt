<template>
    <v-app-bar
        app
        flat
        color="green"
    >
        <v-container green align="left" padding="2px" class="py-0 fill-height">
        <v-avatar
          class="mr-10"
          color="grey darken-1"
          size="32"
        ></v-avatar>
            <v-btn to="/inspire">Inspire</v-btn>
            <v-btn to="/inspire">Inspire</v-btn>
            <v-btn to="/inspire">Inspire</v-btn>
        

        <v-spacer></v-spacer>

        <v-responsive max-width="260">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>
</template>

<script>
export default {
    
  }
</script>