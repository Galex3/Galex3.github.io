<template>
  <section>
    <h2 class="h4 mt-4">Education</h2>
    <div v-for="edu in education" :key="edu.degree" class="mb-3">
      <h5 class="mb-1">{{ edu.degree }}</h5>
      <small class="text-muted">{{ edu.institution }} | {{ edu.year }}</small>
      <ul class="mb-0">
        <li v-for="detail in edu.details" :key="detail">{{ detail }}</li>
      </ul>
    </div>
  </section>
</template>

<script setup>
defineProps(['education'])
</script>
