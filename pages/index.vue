<template lang="pug">
  .page
    section-header(
      title="CaekInc blog"
      subtitle="Помощь для изучения фронта"
    )

    app-options

    post-list
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'HomePage',
})
</script>
