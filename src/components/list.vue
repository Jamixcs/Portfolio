<script setup>
defineProps({
  portfolioProjects: {
    type: Object,
    required: true,
  },
});
</script>
<template>
  <div
    class="flex max-w-4xl flex-wrap items-start justify-center gap-4 text-center"
  >
    <div
      v-for="project in portfolioProjects"
      :key="project.index"
      class="h-[18rem] w-[18rem]"
    >
      <a :href="project.href" :target="project.target" class="hover:opacity-75">
        <img
          :src="project.src"
          :alt="project.alt"
          class="h-[100%] w-[100%] object-cover"
        />
      </a>
    </div>
  </div>
</template>

<style scoped></style>
