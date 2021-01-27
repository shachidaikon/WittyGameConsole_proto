<template>
  <v-container class="fill-height" fluid style="min-height: 434px">
    <v-fade-transition mode="out-in">
      <v-row>
        <v-col v-for="card in cards" :key="card.title" cols="6">
          <v-card>
            <v-img
              :src="card.src"
              max-height="125"
              contain
              class="grey darken-4"
            ></v-img>
            <v-card-title v-text="card.title"> </v-card-title>
            <v-card-subtitle class="pb-0" v-text="card.subtitle">
            </v-card-subtitle>

            <v-card-text
              class="text--primary mt-3"
              style="white-space: pre-wrap"
              v-text="card.text"
            >
            </v-card-text>

            <v-card-actions>
              <v-btn
                v-if="card.link"
                color="rgb(116,166,76)"
                :href="card.link"
                target="_blank"
                text
              >
                VISIT
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-fade-transition>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: '研究室紹介ページ',
        subtitle: 'STUDIOを利用して作成',
        src: 'https://picsum.photos/350/165?random',
        text: 'STUDIOでデザインを担当。',
        link: 'https://keita-lab.jp/OC2020',
      },
      {
        title: 'SkillUpChat',
        subtitle: 'Vue3, Firebase, を用いて制作',
        src: 'https://picsum.photos/350/165?random',
        text: 'モダンなWeb制作技術を学び、',
        link: 'https://skillupchat.web.app/',
      },

      {
        title: 'ポートフォリサイト',
        subtitle: 'Nuxt.js, Vuetify, Netlifyを用いて制作',
        src: 'https://picsum.photos/350/165?random',
        text: '静的サイトということでNuxt.js',
        link: '',
      },
    ],
  }),
}
</script>
