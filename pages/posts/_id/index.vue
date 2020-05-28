<template>
  <div class="card">
    <h2>{{post.title}}</h2>
    <p>Id: {{post.id}}</p>
    <p>Usuario: {{post.userId}}</p>
    <p>Content: {{post.completed}}</p>
  </div>
</template>


<script>
import axios from "axios";
export default {
  data() {
    return {
      post: {}
    };
  },
  async created() {
    try {
      const res = await axios.get(
        "https://jsonplaceholder.cypress.io/todos/" + this.$route.params.id
      );
      this.post = res.data;
    } catch (error) {
      console.error(error);
    }
  }
};
</script>

<style>
.card {
  border: 1px solid whitesmoke;
  padding: 4rem;
}
</style>