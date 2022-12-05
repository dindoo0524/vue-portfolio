<template>
  <div>
    <v-navigation-drawer v-model="drawer" absolute temporary app width="150" height="340">
      <v-list class="pt-4">
        <v-list-tile active-class="green--text" to="/">
          <v-list-tile-content>
            <v-list-tile-title>메인</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="green--text" to="/resume">
          <v-list-tile-content>
            <v-list-tile-title>이력서</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <!-- <v-list-tile active-class="green--text" to="/portfolio">
          <v-list-tile-content>
            <v-list-tile-title>포트폴리오</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile> -->
        <v-list-tile active-class="green--text" href="https://logical-joy.tistory.com/" target="_blank">
          <v-list-tile-content>
            <v-list-tile-title>개발 블로그</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile active-class="green--text" to="/contact">
          <v-list-tile-content>
            <v-list-tile-title>문의</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar flat dense color="transparent" scroll-off-screen>
      <v-toolbar-side-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>
        <a href="/" style="color: inherit; text-decoration: none;">
          <span class="green--text headline">나진주 </span>
          <span class="font-weight-light">Grace</span>
        </a>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn @click="changeTheme" depressed small icon class="hidden-md-and-up">
        <v-icon v-if="goDark==true">fas fa-sun</v-icon>
        <v-icon v-else>fas fa-moon</v-icon>
      </v-btn>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat to="/" active-class="green--text headline">메인</v-btn>
        <v-btn flat to="/resume" active-class="green--text headline">이력서</v-btn>
        <!-- <v-btn flat to="/portfolio" active-class="green--text headline">포트폴리오</v-btn> -->
        <v-btn flat href="https://logical-joy.tistory.com/" target="_blank" active-class="green--text headline">개발 블로그</v-btn>
        <v-btn flat to="/contact" active-class="green--text headline">문의</v-btn>
        <v-btn @click="changeTheme" depressed small icon>
          <v-icon v-if="goDark==true">fas fa-sun</v-icon>
          <v-icon v-else>fas fa-moon</v-icon>
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  props: {
    goDark: {
      type: Boolean
    }
  },
  data () {
    return {
      drawer: null
    }
  },
  methods: {
    changeTheme () {
      this.$emit('changeTheme', this.goDark)
    }
  }
}
</script>

<style >
</style>
