<template>
  <section class="section">
    <div class="content">
      <div class="ep__container">
        <section-header
          :title="errorText.title"
          :subtitle="errorText.subtitle"
        ></section-header>
        <nuxt-link class="ep__link primary" to="/">Home page</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

type Error = {
  statucCode: number
  message: string
}

type ErrorText = {
  title: string
  subtitle: string
}

type ErrorTexts = {
  [key: number]: ErrorText
  default: ErrorText
}

export default Vue.extend({
  name: 'ErrorPage',

  props: {
    error: {
      type: Object as () => Error,
      required: true,
    },
  },

  data: () => ({
    texts: {
      404: {
        title: '404. Page not found',
        subtitle: 'Something went wrong with you',
      },
      default: {
        title: 'Unknow Error',
        subtitle: 'Something wenw wrong with US',
      },
    } as ErrorTexts,
  }),

  computed: {
    errorText(): ErrorText {
      const { statucCode } = this.error
      return this.texts[statucCode] || this.texts.default
    },
  },
})
</script>
