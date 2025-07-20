<template>
  <section id="skills">
    <h2 class="h4 mt-4">Technical Skills</h2>
    <ul class="list-inline">
      <li v-for="skill in skills" :key="skill" class="list-inline-item">
        <span class="badge bg-primary mb-1">{{ skill }}</span>
      </li>
    </ul>
  </section>
</template>

<script setup>
defineProps(['skills'])
</script>
