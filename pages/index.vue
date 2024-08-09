<script setup>
const { data: posts } = await useAsyncData("latest-posts", () =>
  queryContent("/blog").sort({ data: 1 }).limit(3).find()
);
</script>

<template>
  <section>
    <h1 class="text-5xl font-bold mt-20">👋🏻 Hello, I'm Sean Park!</h1>
    <p class="text-2xl text-gray-900 p-2 italic">
      Frontend Developer in Sydney
    </p>
  </section>
  <section class="flex flex-col md:flex-row">
    <img
      src="~/assets/images/profile.webp"
      class="w-full md:w-1/2 max-w-sm p-8 mx-auto md:mx-0 rounded-full"
    />
    <div class="md:w-3/4">
      <h2 class="text-3xl font-bold mt-8">About Me</h2>
      <p class="text-lg py-4 text-gray-700">
        As a recent IT graduate from the University of Technology Sydney, I
        specialize in front-end development with a focus on dynamic and
        responsive web applications. My expertise includes HTML, CSS,
        JavaScript, and frameworks like React and Vue, alongside back-end
        technologies such as Django and .NET. I also have database skills in
        MySQL and PostgreSQL.
      </p>
      <p class="text-lg py-4 text-gray-700">
        Outside of my professional pursuits, I enjoy reading, listening to
        music, and traveling. These activities provide relaxation and
        inspiration, fueling my creativity and curiosity in my work as a
        developer.
      </p>
    </div>
  </section>

  <section>
    <h2 class="text-3xl font-bold mt-8">Latest Blog Posts</h2>
    <div class="grid md:grid-cols-3 pt-8 gap-10">
      <Post :posts="posts" />
    </div>
  </section>
</template>
