<template>
<section :class="`section pb-0`">
  <div class="container">
    <div class="row row-grid" v-for="i in Math.ceil(posts.length / 2)" :key="i">
      <post-card v-for="post in posts.slice((i - 1) * 2, i * 2)" v-bind:key="post.slug" :prefix="prefix" :post="post" :ct="getClassType()"></post-card>
    </div>
  </div>
</section>
</template>

<script>
import PostCard from '~/components/PostCard-web.vue'

export default {
  layout: 'arielle-cerini',
  name: 'Exhibit-web',
  components: {
    PostCard
  },
  props: {
    prefix: String,
    slug: String,
    posts: Array
  }
}
</script>

<style scoped>
.container {
  margin-top: 100px;
  padding-bottom: 100px;
}
</style>