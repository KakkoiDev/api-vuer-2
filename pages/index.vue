<script setup lang="ts">
import { ref } from "vue";

const search = ref("init");
</script>

<template>
  <section>
    <AppTitle />
    <div class="text-lg text-center mt-6">Do you have an API about:</div>
    <SearchInput class="mt-3" v-model="search" />
    {{ search }}
  </section>
  <section>test</section>
</template>
