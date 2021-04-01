<template>
  <section class="section">
    <div class="content">
      <h1 class="sh__title h1">{{ title }}</h1>
      <p class="sh__subtitle body2 regular" v-if="subtitle">{{ subtitle }}</p>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'SectionHeader',

  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      default: '',
    },
  },
})
</script>

<style lang="scss" scoped>
.sh {
  &__title {
    margin: 0;
  }
  &__subtitle {
    color: $text-secondary;
    margin-top: 16px;
  }
}
</style>
