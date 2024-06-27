<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";

const year: Ref<number> = ref(new Date().getFullYear());
</script>

<template>
  <footer class="flex items-center justify-center h-16 space-x-1">
    <LinkOut to="https://www.kakkoi.dev/">KakkoiDev</LinkOut>
    <span> &copy; {{ year }} | </span>
    <LinkOut to="https://github.com/KakkoiDev/api-vuer-2">
      <Icon name="mdi:github" class="h-6 w-6 mr-1" /> Repo
    </LinkOut>
  </footer>
</template>
