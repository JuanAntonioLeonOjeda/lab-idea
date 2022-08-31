<template>
  <div id="app">
    <PostList :posts="postList" />
  </div>
</template>

<script>
import PostList from "@/components/PostList.vue";
var posts = require("./posts.json");
export default {
  name: "App",
  components: {
    PostList,
  },
  data() {
    return {
      postList: posts,
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
