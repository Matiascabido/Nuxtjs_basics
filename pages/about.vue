<template>
  <div>
    <h1>About</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Architecto ullam reprehenderit dolor.</p>
  </div>
</template>



<script>
export default {
  head() {
    return {
      title: "Application Nuxt Post | Home",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Website about posts"
        }
      ],
      htmlAttrs: {
        lang: "en"
      }
    };
  }
};
</script>