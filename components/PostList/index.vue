<template>
  <section class="section">
    <div class="content">
      <p
        class="pl__count-icon"
        src="~/assets/icons/list.svg"
        alt="icon-list"
      ></p>
      Total {{ posts.length }} posts
    </div>
    <div class="pl__items">
      <post-card v-for="post in posts" :key="post.id" :post="post"></post-card>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
import posts from '~/content/posts'

export default Vue.extend({
  name: 'PostList',

  data: () => ({
    posts,
  }),
})
</script>

<style lang="scss" scoped>
section.section {
  margin-top: 32px;
  @media (min-width: $tablet) {
    margin-top: 64px;
  }
}
.pl {
  &__count {
    display: inline-flex;
    align-items: center;
    margin-bottom: 12px;
    color: $text-secondary;
    @media (min-width: $tablet) {
      margin-bottom: 24px;
    }
    &-icon {
      margin-right: 12px;
    }
  }
  &__items {
    margin-top: 12px;
    @media (min-width: $tablet) {
      margin-top: 24px;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: 24px;
    }
  }
}
</style>
