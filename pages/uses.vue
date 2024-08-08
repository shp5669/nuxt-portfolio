<template>
  <section class="uses-section py-16 px-8 bg-gray-100">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold mb-8">
        <i class="fas fa-tools mr-2"></i>What I Use
      </h2>
      <p class="text-xl text-gray-700 mb-12">
        Here is a list of tools, software, and skills I use on a daily basis.
      </p>

      <div class="category">
        <h3 class="text-3xl font-semibold mb-6">
          <i class="fas fa-code mr-2"></i>Development Tools
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <div
            v-for="(tool, index) in developmentTools"
            :key="index"
            class="use-item p-6 bg-white shadow-md rounded-lg"
          >
            <h4 class="text-2xl font-semibold mb-4">{{ tool.name }}</h4>
            <p class="text-gray-600">{{ tool.description }}</p>
          </div>
        </div>
      </div>

      <div class="category mt-12">
        <h3 class="text-3xl font-semibold mb-6">
          <i class="fas fa-layer-group mr-2"></i>Frameworks & Libraries
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <div
            v-for="(framework, index) in frameworks"
            :key="index"
            class="use-item p-6 bg-white shadow-md rounded-lg"
          >
            <h4 class="text-2xl font-semibold mb-4">{{ framework.name }}</h4>
            <p class="text-gray-600">{{ framework.description }}</p>
          </div>
        </div>
      </div>

      <div class="category mt-12">
        <h3 class="text-3xl font-semibold mb-6">
          <i class="fas fa-user-friends mr-2"></i>Soft Skills
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <div
            v-for="(skill, index) in softSkills"
            :key="index"
            class="use-item p-6 bg-white shadow-md rounded-lg"
          >
            <h4 class="text-2xl font-semibold mb-4">{{ skill.name }}</h4>
            <p class="text-gray-600">{{ skill.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const developmentTools = ref([
  {
    name: "Visual Studio Code",

    description:
      "A powerful and customizable code editor that I use for all my development work.",
  },
  {
    name: "Git",
    description:
      "A version control system that helps me manage my code and collaborate with others.",
  },
  {
    name: "GitHub",
    description:
      "A platform for hosting and sharing my code repositories with the world.",
  },
  {
    name: "Figma",
    description:
      "A collaborative design tool that I use for creating wireframes and prototypes.",
  },
  {
    name: "Slack",
    description:
      "A communication platform that I use to stay in touch with my team and manage projects.",
  },
  {
    name: "MacBook Pro",
    description:
      "My main development machine, offering powerful performance and a sleek design.",
  },
]);

const frameworks = ref([
  {
    name: "Vue.js",
    description:
      "A progressive JavaScript framework for building user interfaces and single-page applications.",
  },
  {
    name: "React",
    description:
      "A JavaScript library for building user interfaces, particularly single-page applications.",
  },
  {
    name: "Tailwind CSS",
    description:
      "A utility-first CSS framework that helps me build modern and responsive designs quickly.",
  },
  {
    name: "Bootstrap",
    description:
      "A popular CSS framework for developing responsive and mobile-first websites.",
  },
  {
    name: "Express.js",
    description:
      "A minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.",
  },
  {
    name: "MongoDB",
    description:
      "A NoSQL database that allows for flexible and scalable data storage.",
  },
  {
    name: "Node.js",
    description:
      "A JavaScript runtime that allows me to build scalable and high-performance web applications.",
  },
]);

const softSkills = ref([
  {
    name: "Communication",
    description:
      "Strong verbal and written communication skills, essential for team collaboration and client interactions.",
  },
  {
    name: "Problem-Solving",
    description:
      "Adept at identifying issues and finding creative solutions to complex problems.",
  },
  {
    name: "Time Management",
    description:
      "Excellent time management skills to ensure timely delivery of projects and tasks.",
  },
  {
    name: "Teamwork",
    description:
      "Proven ability to work effectively as part of a team, both as a leader and a collaborator.",
  },
  {
    name: "Adaptability",
    description:
      "Quick to adapt to new technologies and methodologies in a fast-paced environment.",
  },
  {
    name: "Critical Thinking",
    description:
      "Ability to analyze situations and make well-informed decisions.",
  },
]);
</script>

<style scoped>
.uses-section {
  background-color: #f7fafc;
}
.use-item {
  background-color: #ffffff;
}
</style>
