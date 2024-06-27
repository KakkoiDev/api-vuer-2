<script setup lang="ts">
defineProps<{
  to: string;
}>();
</script>

<template>
  <NuxtLink
    :to="to"
    target="_blank"
    class="flex text-blue-600 hover:text-blue-500 transition"
    ><slot
  /></NuxtLink>
</template>
