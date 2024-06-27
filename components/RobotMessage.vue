<script setup lang="ts">
import { computed } from "vue";
import type { RobotState } from "~/types/RobotState";

const props = defineProps<{
  state: RobotState;
}>();

const message = computed<string>(() => {
  if (props.state === "waiting") return "Awaiting search request!";
  if (props.state === "listening") return "Listening...";
  if (props.state === "has results") return "Here are your results!";
  if (props.state === "has no results") return "No results found!";
  return "What!?";
});
</script>

<template>
  <div>
    {{ message }}
  </div>
</template>
