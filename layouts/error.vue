<template lang="pug">
  section.section
    .content
      .ep__container
        section-header(
          :title="errorText.title"
          :subtitle="errorText.subtitle"
        )

        nuxt-link.ep__link(
          class="primary"
          to="/"
        ) Home page
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
