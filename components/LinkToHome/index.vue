<template>
  <section class="section">
    <div class="content">
      <nuxt-link class="lth__link primary" to="/"
        ><img
          class="lth__link-icon"
          src="~assets/icons/home.svg"
          alt="icon-home"
      /></nuxt-link>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'LinkToHome',
})
</script>
