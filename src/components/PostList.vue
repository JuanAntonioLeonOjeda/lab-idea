<template>
  <div class="list">
    <span v-for="post in posts" :key="post.id">
      <PostComponent :post="post" />
    </span>
  </div>
</template>

<script>
import PostComponent from "@/components/PostComponent.vue";

export default {
  name: "PostList",
  props: {
    posts: {
      type: Array,
    },
  },
  components: {
    PostComponent,
  },
};
</script>

<style lang="scss" scoped></style>
