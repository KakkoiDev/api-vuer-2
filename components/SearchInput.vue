<script setup lang="ts">
defineProps<{
  class: string;
  placeholder: string;
}>();

const model = defineModel();
</script>

<template>
  <div class="relative" :class="class">
    <input
      type="text"
      class="rounded-md border-gray-900 px-5 py-3 shadow-sm w-full focus:outline-none placeholder-gray-500"
      v-model="model"
      :placeholder="placeholder"
    />
    <Icon
      name="mdi:close-thick"
      class="absolute top-3 right-4 cursor-pointer w-6 h-6"
      title="Clear Search"
      @click="model = ''"
    />
  </div>
</template>
