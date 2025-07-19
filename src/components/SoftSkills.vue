<template>
  <section>
    <h2 class="h4 mt-4">Soft Skills</h2>
    <ul class="list-inline">
      <li v-for="soft in softSkills" :key="soft" class="list-inline-item">
        <span class="badge bg-secondary mb-1">{{ soft }}</span>
      </li>
    </ul>
  </section>
</template>

<script setup>
defineProps(['softSkills'])
</script>
