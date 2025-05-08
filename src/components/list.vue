<script setup>
defineProps({
  portfolioProjects: {
    type: Object,
    required: true,
  },
});
const posts = [
  {
    id: 1,
    title: "Boost your conversion rate",
    href: "#",
    description:
      "Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.",
    date: "Mar 16, 2020",
    datetime: "2020-03-16",
    category: { title: "Marketing", href: "#" },
    author: {
      name: "Michael Foster",
      role: "Co-Founder / CTO",
      href: "#",
      imageUrl:
        "https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80",
    },
  },
  // More posts...
];
</script>
<template>
  <!-- <div
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
  </div> -->

  <div class="bg-white">
    <div class="mx-auto max-w-5xl px-6 lg:px-8">
      <div
        class="mx-auto mt-6 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 border-t border-gray-200 pt-6 sm:mt-6 sm:pt-6 lg:mx-0 lg:max-w-none lg:grid-cols-3"
      >
        <article
          v-for="project in portfolioProjects"
          :key="project.index"
          class="flex max-w-lg flex-col items-start gap-4"
        >
          <div class="relative aspect-square overflow-hidden rounded-lg">
            <img
              :src="project.src"
              :alt="project.alt"
              class="h-[100%] w-[100%] object-cover transition duration-500 ease-in-out hover:scale-110"
            />
          </div>
          <div class="flex flex-wrap items-center gap-2 text-sm">
            <time class="text-gray-500">{{ project.time }}</time>
          </div>
          <div class="flex flex-wrap gap-2 text-sm">
            <a
              class="relative z-10 rounded-xl bg-gray-300 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-400"
              v-for="(tag, index) in project.tag"
              :key="index"
              >{{ tag }}</a
            >
          </div>
          <div class="group relative flex-auto">
            <h3 class="text-lg/6 font-semibold text-gray-900">
              {{ project.name }}
            </h3>
            <span class="mt-2 text-sm/6 whitespace-pre-line text-gray-600">
              {{ project.team }}
            </span>
            <p class="mt-3 text-sm/6 whitespace-pre-line text-gray-600">
              {{ project.content }}
            </p>
          </div>
          <a
            v-if="project.href"
            :href="project.href"
            :target="project.target"
            class="relative z-10 inline-block transform self-center rounded-md bg-slate-500 px-4 py-2 text-lg text-white transition duration-300 ease-in-out hover:scale-105 hover:bg-slate-600 focus:ring-2 focus:ring-slate-600 focus:ring-offset-2 focus:outline-none md:self-end"
          >
            🔍 查看作品
          </a>
          <a
            v-else
            class="relative z-10 inline-block transform self-center rounded-md bg-slate-500 px-4 py-2 text-lg text-white transition duration-300 ease-in-out hover:scale-105 hover:bg-slate-600 focus:ring-2 focus:ring-slate-600 focus:ring-offset-2 focus:outline-none md:self-end"
          >
            內部系統，未能公開網址
          </a>
        </article>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
