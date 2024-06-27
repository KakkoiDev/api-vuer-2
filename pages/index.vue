<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from "vue";
import type { RobotState } from "~/types/RobotState";

const search: Ref<string> = ref("");
const robotState: Ref<RobotState> = ref("waiting");
</script>

<template>
  <section>
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
