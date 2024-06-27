<template>
  <div class="flex flex-col min-h-screen justify-between">
    <main
      class="w-full px-8 py-12 max-w-6xl mx-auto grid grid-cols-1 gap-7 sm:grid-cols-2"
    >
      <slot />
    </main>
    <AppFooter />
  </div>
</template>
