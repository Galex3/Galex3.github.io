<template>
  <section id="header">
    <h1 class="mb-0">{{ name }}</h1>
    <p class="text-muted">{{ title }}</p>
    <p>{{ summary }}</p>
  </section>
</template>

<script setup>
defineProps(['name', 'title', 'summary'])
</script>
