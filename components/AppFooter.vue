<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";

const year: Ref<number> = ref(new Date().getFullYear());
</script>

<template>
  <footer class="flex items-center justify-center h-16 space-x-1">
    <a
      href="https://www.kakkoi.dev/"
      target="_blank"
      rel="noopener"
      class="text-blue-600 hover:text-blue-500 transition"
    >
      KakkoiDev</a
    >
    <span> &copy; {{ year }} | </span>
    <a
      href="https://github.com/KakkoiDev/api-vuer-2"
      target="_blank"
      rel="noopener"
      class="text-blue-600 hover:text-blue-500 transition flex"
    >
      <Icon name="mdi:github" class="h-6 w-6 mr-1" />
      Repo</a
    >
  </footer>
</template>
