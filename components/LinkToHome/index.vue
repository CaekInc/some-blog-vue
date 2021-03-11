<template lang="pug">
section.section
  .content
    nuxt-link.lth__link(
      to="/"
      class="primary"
    )
      img.lth__link-icon(
        src="~assets/icons/home.svg"
        alt="icon-home"
      )
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'LinkToHome',
})
</script>
