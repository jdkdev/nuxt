<template id="nav-bar">
    <div>
      <nuxt-link
          v-for="post in posts"
          :to="{name: 'posts-id', params: {id: post.id}}"
          :key="post.id"
          class="button--grey"
        >
          {{post.title}}
        </nuxt-link>
    </div>

</template>
<script charset="utf-8">
export default {
  components: {
  },
  computed: {
    posts () {
      return this.$store.state.posts.all
    }
  }
}
</script>
</script>
