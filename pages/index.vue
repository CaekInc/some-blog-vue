<template lang="pug">
  .page
    section-header(
      title="Caek blog"
      subtitle="Some front-end features for me"
    )

    post-list
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'HomePage',
})
</script>
