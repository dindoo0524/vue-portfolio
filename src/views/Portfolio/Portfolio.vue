<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg4 xl4>
        <v-card
          :to="'/portfolio/web'"
          hover
          height="280"
        >
          <v-card-title></v-card-title>
          <v-img :src="require('@/assets/web_developer.png')" class="mx-auto" height="180" center cover></v-img>
          <v-card-title primary-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>Web 개발 프로젝트</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm12 md4 lg4 xl4>
        <v-card
          :to="'/portfolio/app'"
          hover
          height="280"
        >
          <v-card-title></v-card-title>
          <v-img :src="require('@/assets/app.png')"  class="mx-auto" height="180" cover></v-img>
          <v-card-title primary-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>App 개발 프로젝트</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Portfolio',
    titleTemplate: "%s ← Grace's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Grace's Portfolio Web Development Video Editing Graphic Design Front-End Advetising"
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Grace' Space" },
      { property: 'og:site_name', content: "Grace' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://dindoo0524.github.io' },
      {
        property: 'og:image',
        content: 'https://i.imgur.com/Dcz2PGx.jpg'
      },
      {
        property: 'og:description',
        content:
          "Grace's Portfolio Web Development Video Editing Graphic Design Front-End Advetising"
      }
    ]
  },
  data () {
    return {
      portfolios: [
        {
          src: '@/assets/web.png',
          title: 'Web'
        },

        {
          src: '@/assets/app.png',
          title: 'App'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
