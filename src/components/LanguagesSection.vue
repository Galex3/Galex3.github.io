<template>
  <section id="languages">
    <h2 class="h4 mt-4">Languages</h2>
    <ul>
      <li v-for="lang in languages" :key="lang.name">{{ lang.name }} - {{ lang.level }}</li>
    </ul>
  </section>
</template>

<script setup>
defineProps(['languages'])
</script>
