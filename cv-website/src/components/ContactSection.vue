<template>
  <section>
    <p>
      <strong>Email:</strong> <a :href="'mailto:' + contact.email">{{ contact.email }}</a><br />
      <strong>Phone:</strong> <a :href="'tel:' + contact.phone.replace(/\s/g, '')" target="_blank">{{ contact.phone }}</a><br />
      <strong>Location:</strong> {{ contact.location }}<br />
      <strong>LinkedIn:</strong> <a :href="contact.linkedin" target="_blank">linkedin.com/in/galexs</a><br />
      <strong>GitHub:</strong> <a :href="contact.github" target="_blank">github.com/Galex3</a>
    </p>
  </section>
</template>

<script setup>
defineProps(['contact'])
</script>

<style lang="css" scoped>
  a {
    text-decoration: none;
  }
</style>