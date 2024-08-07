<script setup>
const { data: posts } = await useAsyncData("latest-posts", () =>
  queryContent("/blog").sort({ data: 1 }).limit(3).find()
);
</script>

<template>
  <section>
    <h1 class="text-5xl font-bold mt-20">👋🏻 Hello, I'm Sean Park!</h1>
    <p class="text-base text-gray-900 p-2 italic">
      MERN Stack Developer in Sydney
    </p>
  </section>
  <section class="flex flex-col md:flex-row">
    <div class="md:w-3/4">
      <h2 class="text-3xl font-bold mt-8">My Story</h2>
      <p class="text-lg py-4 text-gray-700">
        I am an IT graduate from the University of Technology Sydney with a
        specialization in front-end development. My expertise lies in web
        application creation and seamless system integration, allowing me to
        thrive on the cutting edge of software development. Fluent in multiple
        programming languages, I am passionate about diving into innovative
        projects, solving problems creatively, and delivering robust solutions.
      </p>
      <p class="text-lg py-4 text-gray-700">
        Professionally, I’ve contributed to various innovative projects with a
        keen focus on web programming. Currently, I’m immersed in projects
        utilizing the JavaScript stack, leveraging my skills in MongoDB,
        Express.js, React, and Node.js to deliver robust solutions.
      </p>
      <p class="text-lg py-4 text-gray-700">
        Outside the tech realm, I channel my enthusiasm into reading, listening
        to music, and traveling. Whether I’m getting lost in a captivating book,
        discovering new music, or exploring new destinations, I bring the same
        energy and curiosity to my personal life.
      </p>
    </div>
    <img
      src="~/assets/images/profile.webp"
      class="w-full md:w-1/2 max-w-sm p-8 mx-auto md:mx-0 rounded-full"
    />
  </section>

  <section>
    <h2 class="text-3xl font-bold mt-8">Latest Blog Posts</h2>
    <div class="grid md:grid-cols-3 pt-8 gap-10">
      <Post :posts="posts" />
    </div>
  </section>
</template>
