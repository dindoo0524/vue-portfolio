<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <v-img
      :src="require('../assets/profile.png')"
      width="700px"
      height="400px"
      alt="나진주 프로필 사진"
      lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
      cover
    ></v-img>

    <br>

    <vue-typer class="headline" :repeat="0" text="4년차 프론트엔드 + 앱 개발자 나진주"></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">
              <span>About</span>
              <span class="green--text">Me</span>
            </h3>
            <div>
              <p>
                안녕하세요!
                저는
                <span
                  class="green--text font-weight-bold"
                >
                프론트엔드 개발(Vue.js, React.js, Nuxt.js)
                </span>
                및
                <span
                  class="green--text font-weight-bold"
                >
                앱 개발(React-Native, Flutter)
                </span>
                을 하고 있는 4년차 개발자입니다!
              </p>
            </div>
            <div>
              <p>
                저는 배움에 열정을 가지고, 또 배운것들을 나누는데 즐거움을 느끼는
                <br/>
                <span
                  class="green--text font-weight-bold"
                >
                Programming Eudcator
                </span>
                이기도 합니다.

              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from 'vue-typer'

export default {
  metaInfo: {
    title: 'Home',
    titleTemplate: "%s ← Grace's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'description', content: "Grace's Portfolio" },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Grace' Space" },
      { property: 'og:site_name', content: "Grace' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://dindoo0524.github.io' },
      {
        property: 'og:image',
        content: 'https://i.imgur.com/Dcz2PGx.jpg'
      },
      { property: 'og:description', content: "Grace's Portfolio" }
    ]
  },
  components: {
    'vue-typer': VueTyper
  },
  data () {
    return {
      icons: [
        { href: 'https://github.com/dindoo0524', icon: 'fab fa-github' },
        {
          href: 'https://www.linkedin.com/in/%EC%A7%84%EC%A3%BC-%EB%82%98-40174b229/',
          icon: 'fab fa-linkedin-in'
        },
        { href: 'https://apps.apple.com/kr/app/%EB%91%90%EC%8D%A8%ED%82%B7-%EB%9D%BC%EC%9D%B4%EB%B8%8C/id1541099596', icon: 'fab fa-app-store-ios' },
        { href: 'https://play.google.com/store/apps/details?id=com.smartfitkorea.smartpass', icon: 'fab fa-google-play' },
        { href: 'http://wlswnwhro95.cafe24.com/', icon: 'fas fa-folder-open' },
        {
          href: 'https://www.facebook.com/wlswnwhro95',
          icon: 'fab fa-facebook-f'
        },
        { href: 'https://www.instagram.com/dev._.rabbit', icon: 'fab fa-instagram' },
        { href: 'https://logical-joy.tistory.com', icon: 'fas fa-pen-nib' },
        { href: 'https://joyful-coding.liveklass.com', icon: 'fas fa-play-circle' }
      ],
      text1: ['Front-End Developer', 'Mobile Application Developer'],
      leftImage: 'https://i.imgur.com/bU50uS9.jpg',
      rightImage: 'https://i.imgur.com/z3ZoEEw.jpg',
      leftImage2: 'https://i.imgur.com/SXBitjh.jpg',
      rightImage2: 'https://i.imgur.com/Dcz2PGx.jpg',
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    }
  }
}
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: green;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: green;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
