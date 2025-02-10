<script setup>
import Header from "./header.vue";
import List from "./list.vue";
</script>

<template>
  <main class="wrap">
    <Header />
    <List />
  </main>
</template>

<style scoped>
.wrap {
  margin: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
