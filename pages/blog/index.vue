<script setup>
const { data: posts } = await useAsyncData("posts", () =>
  queryContent("/blog").find()
);
</script>

<template>
  <h1 class="text-3xl my-8">Blog Posts</h1>

  <p class="text-lg text-gray-900 italic my-8">
    I like to write about anything that I am currently working or something new
    that interests me.
  </p>

  <section class="grid md:grid-cols-3 mt-32 gap-10">
    <Post :posts="posts" />
  </section>
</template>
