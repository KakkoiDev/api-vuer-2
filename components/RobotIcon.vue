<script setup lang="ts">
import type { RobotState } from "~/types/RobotState";

defineProps<{
  state: RobotState;
}>();
</script>

<template>
  <Icon v-if="state === 'waiting'" name="mdi:robot-outline" class="h-40 w-40" />
  <Icon
    v-else-if="state === 'searching'"
    name="mdi:robot-excited-outline"
    class="h-40 w-40"
  />
  <Icon
    v-else-if="state === 'has no results'"
    name="mdi:robot-dead-outline"
    class="h-40 w-40"
  />
  <Icon
    v-else-if="state === 'has results'"
    name="mdi:robot-happy-outline"
    class="h-40 w-40"
  />
  <Icon v-else name="mdi:robot-confused-outline" class="h-40 w-40" />
</template>
