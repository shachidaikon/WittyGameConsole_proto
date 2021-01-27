<template>
  <v-row justify="center" align="start">
    <v-col cols="12">
      <v-carousel cycle hide-delimiters :show-arrows="false" height="350">
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
          height="350"
        >
        </v-carousel-item>
      </v-carousel>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: require('../assets/champion.png'),
        },
        {
          src: require('../assets/dogcat.png'),
        },
        {
          src: require('../assets/murabito.png'),
        },
      ],
    }
  },
}
</script>
