<template>
  <section class="section">
    <div class="content">
      <div class="app-options">
        <switcher-color-mode></switcher-color-mode>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'AppOptions',
})
</script>

<style lang="scss" scoped>
.app-options {
  display: flex;
  margin-top: 24px;
}
</style>
