<script setup>
defineProps({
  portfolioTitle: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <h1 class="m-[20px] text-center text-4xl">{{ portfolioTitle }}</h1>
</template>

<style scoped></style>
