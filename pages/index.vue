<template>
  <v-container>
    <v-row justify="center" align-content="center" style="height: 350px">
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
          News
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
          Slides
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
          Friend
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
          Chat
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="cyan"
          href="https://www.google.com/?hl=ja"
          elevation="10"
        >
          Hint
        </v-btn>

        <v-btn
          class="mx-4"
          fab
          dark
          x-large
          color="purple"
          href="https://meet.google.com/kcp-wcot-zgf"
          elevation="10"
        >
          video
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
