<template>
  <div>
    <h1>Posts</h1>
    <Post v-for="post of posts" :key="post.id" :name="post.title" :id="post.id" />
  </div>
</template>

<script>
import axios from "axios";
import Post from "../../components/Post";
export default {
  components: {
    Post
  },
  data() {
    return {
      posts: []
    };
  },
  async created() {
    try {
      const res = await axios.get("https://jsonplaceholder.cypress.io/todos");
      this.posts = res.data;
    } catch (error) {
      console.log(error);
    }
  }
};
</script>