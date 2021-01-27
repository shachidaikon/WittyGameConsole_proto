<template>
  <v-container>
    <v-row justify="center" align-content="center" style="height: 350px">
      <v-col
        cols="12"
        justify="center"
        class="text-center"
        style="color: rgb(116, 166, 76); font-weight: bold; font-size: 80px"
      >
        Witty Game Console
      </v-col>
      <v-col cols="12" justify="center" class="text-center">
        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="primary"
          to="/News"
          elevation="10"
        >
          <v-icon>mdi-information</v-icon>
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="pink"
          to="/Carousels"
          elevation="10"
        >
          <v-icon>mdi-camera-burst</v-icon>
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="indigo"
          to="/Friend"
          elevation="10"
        >
          <v-icon>mdi-account-multiple</v-icon>
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="teal"
          to="/News"
          elevation="10"
        >
          <v-icon>mdi-chat-processing</v-icon>
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="cyan"
          href="https://www.youtube.com/?gl=JP&tab=r1"
          elevation="10"
        >
          <v-icon>mdi-youtube</v-icon>
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="purple"
          href="https://meet.google.com/ihb-qpbm-ane"
          elevation="10"
        >
          <v-icon>mdi-video</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  },
}
</script>
