<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app color="rgb(249,249,249)">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <v-toolbar-title class="colorrize" v-text="title" />
    </v-app-bar>
    <v-main class="whitenize">
      <v-container>
        <transition name="page">
          <nuxt />
        </transition>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Carousels',
          to: '/Carousels',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'News',
          to: '/News',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Friend',
          to: '/Friend',
        },
      ],
      miniVariant: false,
      title: 'Witty Game Console',
    }
  },
}
</script>

<style lang="scss" scoped>
.colorrize {
  color: rgb(116, 166, 76);
  font-weight: bold;
}
.whitenize {
  background-color: rgb(249, 249, 249);
}
</style>
