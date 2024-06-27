<script setup lang="ts">
import { ref, watch } from "vue";
import type { Ref } from "vue";
import type { RobotState } from "~/types/RobotState";

const {
  data: searchData,
  pending: searchPending,
  error: searchError,
  execute: executeSearch,
} = await useFetch("https://apilist.fun/api/v1/search", {
  query: {
    s: "robot",
  },
  // immediate: false,
  watch: false,
});

const search: Ref<string> = ref("");
const robotState: Ref<RobotState> = ref("waiting");

watch(search, () => {
  console.log("search", search.value);
});
</script>

<template>
  <section>
    <button @click="executeSearch">test</button>
    <AppTitle />
    <div class="text-lg text-center mt-6">Do you have an API about:</div>
    <SearchInput class="mt-3" v-model="search" placeholder="ex: robot" />
    <div class="flex flex-col items-center mt-6">
      <RobotIcon :state="robotState" />
      <RobotMessage :state="robotState" />
      {{ robotState }}
    </div>
  </section>
  <section>test</section>
</template>
