<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";

const search: Ref<string> = ref("");
</script>

<template>
  <section>
    <AppTitle />
    <div class="text-lg text-center mt-6">Do you have an API about:</div>
    <SearchInput class="mt-3" v-model="search" placeholder="ex: robot" />
  </section>
  <section>test</section>
</template>
