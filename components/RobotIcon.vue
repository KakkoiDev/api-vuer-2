<script setup lang="ts">
import type { RobotState } from "~/types/RobotState";

defineProps<{
  state: RobotState;
}>();
</script>

<template>
  <Icon
    v-if="state === 'waiting' || state === 'has results'"
    name="mdi:robot-outline"
    class="h-36 w-36"
  />
  <Icon
    v-else-if="state === 'searching'"
    name="mdi:robot-excited-outline"
    class="h-36 w-36"
  />
  <Icon
    v-else-if="state === 'has no results'"
    name="mdi:robot-dead-outline"
    class="h-36 w-36"
  />
  <Icon v-else name="mdi:robot-confused-outline" class="h-36 w-36" />
</template>
