<template>
  <v-container class="fill-height" fluid style="min-height: 434px">
    <v-fade-transition mode="out-in">
      <v-row>
        <v-col v-for="card in cards" :key="card.title" cols="6">
          <v-card>
            <v-img
              :src="card.src"
              height="175"
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
        title: 'Apex Legends',
        subtitle: 'シーズン8の情報解禁!',
        src: require('../assets/Apex_season8.jpeg'),
        text: '新キャラ、ヒューズの全アビリティが判明!!',
        link:
          'https://www.ea.com/ja-jp/games/apex-legends/season-8?isLocalized=true&setLocale=ja-jp',
      },
      {
        title: 'Little Nightmares Ⅱ',
        subtitle: '悪夢が帰ってくる...',
        src: require('../assets/Little Nightmares ll.jpg'),
        text: '体験版好評配信中!! 発売日は2月10,11日!!',
        link: 'https://n6ls.bn-ent.net/',
      },

      {
        title: 'GeForce NOW',
        subtitle: 'あのゲームからこのゲームまで遊び放題!?',
        src: require('../assets/GeForce NOW.jpg'),
        text: '全キャリア対応クラウドゲーミングサービスがついに上陸!!',
        link:
          'https://cloudgaming.mb.softbank.jp/?utm_source=google&utm_medium=cpc&utm_campaign=gkt_big_device&utm_content=sin&_adp_c=wa&_adp_e=c&_adp_u=p&_adp_p_md=4542&_adp_p_cp=103246&_adp_p_agr=8823905&_adp_p_ad=15432837&gclid=CjwKCAiAu8SABhAxEiwAsodSZKKAGh6WDL69v2FgqxzE90Ge0Y5E5hd7TEfYZrRe6DPrcCrY_4av2xoCkGgQAvD_BwE',
      },
      {
        title: 'DARK SOULS REMASTERED',
        subtitle: '世界中を熱狂させたゲームが半額!!',
        src: require('../assets/DARK SOULS.jpg'),
        text: '期間限定で特別価格に。見逃すな!!',
        link:
          'https://store.steampowered.com/app/570940/DARK_SOULS_REMASTERED/?l=japanese',
      },
    ],
  }),
}
</script>
