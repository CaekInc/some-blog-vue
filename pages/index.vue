<template>
  <div class="page">
    <section-header
      title="CaekInc blog"
      subtitle="Помощь для изучения фронта"
    ></section-header>
    <app-options></app-options>
    <post-list></post-list>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'HomePage',
})
</script>
