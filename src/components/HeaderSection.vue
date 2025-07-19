<template>
  <header>
    <h1 class="mb-0">{{ name }}</h1>
    <p class="text-muted">{{ title }}</p>
    <p>{{ summary }}</p>
  </header>
</template>

<script setup>
defineProps(['name', 'title', 'summary'])
</script>
