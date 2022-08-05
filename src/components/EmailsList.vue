<script setup>
const props = defineProps({
emails: {
    type: Array,
    default: () => ["1","2","3"]
  }
})
</script>

<template>
  <div class="emails-container">
    <h3>Emails: </h3>
    <p>{{ emails.join(", ") }}</p>
  </div>
</template>

<style scoped>
.emails-container {
  margin-bottom: 1rem;
}
h3 {
  font-size: 1.2rem;
}
</style>
