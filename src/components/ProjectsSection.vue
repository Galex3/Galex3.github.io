<template>
  <section>
    <h2 class="h4 mt-4">Projects</h2>
    <div v-for="project in projects" :key="project.name" class="mb-3">
      <h5 class="mb-1">{{ project.name }}</h5>
      <p class="mb-1">{{ project.description }}</p>
      <a v-if="project.link !== '#'" :href="project.link" target="_blank">View Project</a>
    </div>
  </section>
</template>

<script setup>
defineProps(['projects'])
</script>
