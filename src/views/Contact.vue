<template>
  <v-container grid-list-xl>
    <v-layout row align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md6 lg6 xl6>
        <h2 class="pb-4 mt-2">
          <span>연락 주세요 😎</span>
        </h2>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="green" left>fas fa-map-marker-alt</v-icon>
          <span>서울&nbsp;</span>
          <span class="green--text">대한민국</span>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="green" left>fas fa-envelope</v-icon>
          <a href="mailto:jinju@liveklass.com">
            <span>jinju@liveklass.com</span>
          </a>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon large color="green" left>fas fa-phone</v-icon>
          <span class="green--text">010-2727-6548</span>
        </div>
         <div class="py-4 subheading font-weight-bold">
          <v-icon large color="green" left>fab fa-instagram</v-icon>
          <span>Instargram DM&nbsp;</span>
          <a href="https://www.instagram.com/dev._.rabbit" target="_blank" class="green--text">@dev._.rabbit</a>
        </div>
      </v-flex>
      <v-img :src="require('@/assets/happy.png')" class="mx-auto my-auto" center cover></v-img>
    </v-layout>
  </v-container>
</template>

<script>
import { validationMixin } from 'vuelidate'
import {
  required,
  maxLength,
  email,
  minLength
} from 'vuelidate/lib/validators'
export default {
  metaInfo: {
    title: 'Contact',
    titleTemplate: "%s ← Grace's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Grace's Contact Doboj Bosnia and Herzegovina Freelance Get in Touch ContactMe"
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
          "Grace's Contact Doboj Bosnia and Herzegovina Freelance Get in Touch ContactMe"
      }
    ]
  },
  mixins: [validationMixin],
  validations: {
    name: { required, maxLength: maxLength(20) },
    email: { required, email },
    body: { required, minLength: minLength(20) }
  },
  data () {
    return {
      name: '',
      email: '',
      body: ''
    }
  },
  methods: {
    submit () {
      this.$v.$touch()
    },
    clear () {
      this.$v.$reset()
      this.name = ''
      this.email = ''
      this.body = ''
    }
  },
  computed: {
    nameErrors () {
      const errors = []
      if (!this.$v.name.$dirty) return errors
      !this.$v.name.maxLength &&
        errors.push('Name must be at most 20 characters long')
      !this.$v.name.required && errors.push('Name is required.')
      return errors
    },
    emailErrors () {
      const errors = []
      if (!this.$v.email.$dirty) return errors
      !this.$v.email.email && errors.push('Must be valid e-mail')
      !this.$v.email.required && errors.push('E-mail is required')
      return errors
    },
    bodyErrors () {
      const errors = []
      if (!this.$v.body.$dirty) return errors
      !this.$v.body.minLength &&
        errors.push('Text must be at least 20 characters long')
      !this.$v.body.required && errors.push('Text is required')
      return errors
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
