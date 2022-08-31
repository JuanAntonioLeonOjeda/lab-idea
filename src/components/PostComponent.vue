<template>
  <div class="post">
    <h1>{{ post.text }}</h1>
    <br />
    <label for="author">Author: {{ post.author }}</label>
    <br />
    <label for="likes">Likes: {{ countLikes }}</label>
    <br />
    <ButtonComponent text="Like" :addLike="like" />
    <ButtonComponent text="Comment" />
    <ButtonComponent text="Favourites" />
  </div>
</template>

<script>
import ButtonComponent from "@/components/ButtonComponent.vue";

export default {
  name: "PostComponent",
  data() {
    return {
      likes: this.post.likes,
    };
  },
  props: {
    post: {
      type: Object,
    },
  },
  components: {
    ButtonComponent,
  },
  methods: {
    like() {
      this.likes++;
    },
  },
  computed: {
    countLikes() {
      return this.likes;
    },
  },
};
</script>

<style lang="scss" scoped>
.post {
  border: black solid 1px;
  width: 300px;
  height: 120px;
}
h1 {
  margin: 0;
}
</style>
