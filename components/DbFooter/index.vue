<template>
  <section class="section">
    <div class="content">
      <div class="footer">
        <a class="secondary" href="mailto:example@mail.com?subject=Nuxt blog"
          >Contact us</a
        >
        <p class="footer__copyright body3 regular">{{ copyright }}</p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'DbFooter',

  computed: {
    copyright(): string {
      const year = new Date().getUTCFullYear()
      return ` ${year} · All rights reserved`
    },
  },
})
</script>

<style lang="scss" scoped>
.footer {
  margin: $section-indent-mobile 0;
  @media (min-width: $tablet) {
    margin: $section-indent-desktop 0;
  }
  &__copyright {
    margin-top: 16px;
    color: $text-secondary;
  }
}
</style>
