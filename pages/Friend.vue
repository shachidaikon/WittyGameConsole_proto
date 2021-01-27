<template>
  <v-card max-width="450" class="mx-auto">
    <v-list three-line>
      <template v-for="(item, index) in items">
        <v-subheader
          v-if="item.header"
          :key="item.header"
          v-text="item.header"
        ></v-subheader>

        <v-divider
          v-else-if="item.divider"
          :key="index"
          :inset="item.inset"
        ></v-divider>

        <v-list-item v-else :key="item.title">
          <v-list-item-avatar>
            <v-img :src="item.avatar"></v-img>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title v-html="item.title"></v-list-item-title>
            <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    items: [
      { header: 'オンラインのフレンド' },
      {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
        title: 'Mario_is_a_pen',
        subtitle: `<span class="text--primary">オンライン</span> &mdash; Apex Legendsをプレイ中`,
      },
      { divider: true, inset: true },
      {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
        title: 'GOD_OMUTSU',
        subtitle: `<span class="text--primary">オンライン</span> &mdash; Persona5をプレイ中`,
      },
      { divider: true, inset: true },
      {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
        title: 'shachidaikon55',
        subtitle:
          '<span class="text--primary">オンライン</span> &mdash; Apex Legendsをプレイ中',
      },
      { divider: true, inset: true },
      {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/4.jpg',
        title: 'kimushinhan_0206',
        subtitle:
          '<span class="text--primary">オンライン</span> &mdash; Fall Guysをプレイ中',
      },
      { divider: true, inset: true },
      {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg',
        title: 'sunagimo_lover07',
        subtitle:
          '<span class="text--primary">オンライン</span> &mdash; Apex Legendsをプレイ中.',
      },
    ],
  }),
}
</script>
