<template>
  <main class="py-12 max-w-6xl mx-auto grid grid-cols-1 gap-7 sm:grid-cols-2">
    <section>
      <slot name="left-column" />
    </section>
    <section>
      <slot name="right-column" />
    </section>
  </main>
  <AppFooter />
</template>
