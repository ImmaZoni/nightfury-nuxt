<template>
  <v-row class="d-flex justify-center">
    <v-col cols="12" sm="8" md="6">
      <!--- About Us -->
      <v-container class="d-inline justify-center">
        <h1 class="text-center">A Little About Us</h1>
        <p class="text-center">We are an up and coming animal sanctuary based in Phoenix, Arizona striving to help all the animals we can. We are currently working with a limited capacity, but will continue to help every animal in any way possible. We will update our website with the progression of our non profit. For all inquiry's and questions you may contact us at anytime at Admin@thecircleoflifesanctuary.org Please stay tuned for more updates, thank you for all your donations and support!</p>
        <v-btn text absolute color="black">Learn More</v-btn>
      </v-container>
      <v-spacer></v-spacer>
      <!--- Help Us -->
      <v-container class="d-inline justify-center">
        <h1 class="text-center">Help us Make a Difference!</h1>
        <p class="text-center">We need to expand our space to help more animals. There are so many animals out there that we, as well as many other rescues facilities, cannot help due to the lack of space for them. At this time it is our goal to open a larger facility in order to help more animals in desperate need. We could use your help to really make a difference! </p>
        <v-row class="align-center">
          <v-col>
            <v-btn text absolute color="black">Donation Link 1</v-btn>
          </v-col>
          <v-col>
            <v-btn text absolute color="black">Donation Link 2</v-btn>
          </v-col>
        </v-row>
        
      </v-container>
      <v-spacer></v-spacer>
      <!--- Animal Spotlight -->
      <v-container class="d-inline justify-center">
        <h1 class="text-center">A Little About Us</h1>
        <p class="text-center">We are an up and coming animal sanctuary based in Phoenix, Arizona striving to help all the animals we can. We are currently working with a limited capacity, but will continue to help every animal in any way possible. We will update our website with the progression of our non profit. For all inquiry's and questions you may contact us at anytime at Admin@thecircleoflifesanctuary.org Please stay tuned for more updates, thank you for all your donations and support!</p>
        <v-btn text absolute color="black">Learn More</v-btn>
      </v-container>
      <v-spacer></v-spacer>
    </v-col>
  </v-row>
</template>
<style>
.h1 {
  text-align: center;
}
</style>
<script>
export default {
  layout: 'home',
  // OR
  layout (context) {
    return 'home'
  }
}
</script>
