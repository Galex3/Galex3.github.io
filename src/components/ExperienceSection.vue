<template>
  <section id="experience">
    <h2 class="h4">Experience</h2>
    <div v-for="job in experience" :key="job.role" class="mb-3">
      <h5 class="mb-1">
        {{ job.role }} <small class="text-muted">@ {{ job.company }}</small>
      </h5>
      <small class="text-muted">{{ job.duration }}</small>
      <p class="mb-0">{{ job.description }}</p>
    </div>
  </section>
</template>

<script setup>
defineProps(['experience'])
</script>
