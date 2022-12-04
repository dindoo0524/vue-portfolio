<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">경력사항 (3년 3개월)</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">2021년 5월 -</div>
                <div class="caption font-weight-bold green--text">현재(1년 8개월)</div>
              </v-flex>
              <v-flex class="pl-2">
                <a href="https://about.liveklass.com" target="_blank">
                  <v-img
                    :src="require('../assets/futureschole.png')"
                    width="50px"
                    height="50px"
                    alt="futureschole"
                    cover
                  ></v-img>
                </a>
                <strong>(주)퓨쳐스콜레</strong> 프론트엔드 개발자
                <div class="caption mb-2">
                  누구나 쉽게 자신의 지식을 판매할 수 있는 지식 비즈니스 플랫폼 <a href="https://www.liveklass.com/" traget="_blank" class="orange--text">라이브클래스</a>를 서비스 개발
                </div>
                <div class="mb-2">
                  Vue.js, Nuxt.js, Typescript, tailwind, UnitTest(TDD)
                </div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">2020년 2월 -</div>
                <div class="caption font-weight-bold green--text">2021년 5월(1년 4개월)</div>
              </v-flex>
              <v-flex class="pl-2">
                <a href="http://smartfitkorea.com" target="_blank">
                  <v-img
                    :src="require('../assets/smartfit.png')"
                    width="50px"
                    height="50px"
                    alt="smartfit"
                    cover
                  ></v-img>
                </a>
                <strong>(주)스마트핏</strong> 풀스텍 + 앱 개발자
                <div class="caption mb-2">인터넷 헬스케어 전문 교육 및 마케팅 전문 기업</div>
                <div class="caption mb-2">(앱)두써킷 라이브, (앱)스마트짐, (앱)스마트패스, (웹)두써킷 심박시스템 및 관리자 페이지 개발</div>
                <div class="mb-2">React.js, React-Native, node.js, php, Material-UI</div>
                <a href="http://wlswnwhro95.cafe24.com/" target="_blank" class="mb-2">프로젝트 포트폴리오 링크</a>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">2019년 10월 -</div>
                <div class="caption font-weight-bold green--text">2019년 12월(3개월)</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>디벨럽 퍼스트</strong>
                <div class="caption mb-2">채무 관리 프로그램 개발자</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">수상이력</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">2021년 12월</div>
              </v-flex>
              <v-flex class="pl-2">
                <a href="https://nomadcoders.co/" target="_blank">
                  <v-img
                    :src="require('../assets/nomadcoders.png')"
                    width="50px"
                    height="50px"
                    alt="nomadcoders"
                    contain
                  ></v-img>
                </a>
                <strong>Nomad Corder - Mobile App Contest (우수상)</strong>
                <div class="caption mb-2">React-Native와 Expo 및 pixabay api를 사용하여 이미지 검색앱 개발</div>
                <a href="https://expo.dev/@dindoo/pikabey " target="_blank" class="mb-2">Expo 앱 링크</a>
                <br/>
                <a href="https://nomadcoders.co/community/thread/1415" target="_blank">참여 게시글</a>
                <v-img
                    :src="require('../assets/app_contest.png')"
                    width="280px"
                    height="350px"
                    alt="app contest"
                    contain
                  ></v-img>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Programming</span>
          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>Vue/Nuxt</strong>
        <v-progress-linear v-model="buffer11" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Typescript</strong>
        <v-progress-linear v-model="buffer12" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>React</strong>
        <v-progress-linear v-model="buffer13" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>React-Native</strong>
        <v-progress-linear v-model="buffer14" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Flutter</strong>
        <v-progress-linear v-model="buffer15" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>node.js</strong>
        <v-progress-linear v-model="buffer16" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>php</strong>
        <v-progress-linear v-model="buffer17" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <!-- <span>Tools</span> -->
          <span class="green--text">Tools</span>
        </h2>
        <br>
        <strong>Figma</strong>
        <v-progress-linear v-model="buffer21" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Photoshop</strong>
        <v-progress-linear v-model="buffer22" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Zeplin</strong>
        <v-progress-linear v-model="buffer23" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <!-- <div class="mt-4 pt-2">
        <v-btn
          href="https://docs.google.com/document/d/1WSR42FEgUahJuR_RArW1wz7TfUBlgj13zekRidmQgs4/edit?usp=sharing"
          target="_blank"
          color="green"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div> -->
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Resume',
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Eldin' Space" },
      { property: 'og:site_name', content: "Eldin' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://eldin.space' },
      {
        property: 'og:image',
        content: 'https://i.imgur.com/Dcz2PGx.jpg'
      },
      {
        property: 'og:description',
        content:
          'Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End'
      }
    ]
  },
  data () {
    return {
      value: 0,
      buffer11: 0,
      buffer12: 0,
      buffer13: 0,
      buffer14: 0,
      buffer15: 0,
      buffer16: 0,
      buffer17: 0,
      buffer21: 0,
      buffer22: 0,
      buffer23: 0,
      bufferValue: 100,
      interval: 0
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer11 = 85
        this.buffer12 = 75
        this.buffer13 = 80
        this.buffer14 = 70
        this.buffer15 = 60
        this.buffer16 = 80
        this.buffer17 = 70
        this.buffer21 = 95
        this.buffer22 = 85
        this.buffer23 = 90
      }, 800)
    }
  }
}
</script>
<style >
</style>
