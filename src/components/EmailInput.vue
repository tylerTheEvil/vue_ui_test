<script setup>
import { ref } from 'vue'
import EmailsList from './EmailsList.vue';

let newEmail = ref('')
const emails = ref([])

const pushItem = (e) => {
  e.preventDefault()

  emails.value.push(newEmail.value)
  newEmail.value = ''
}
</script>

<template>
  <div class="emails">
    <EmailsList :emails='emails' />
    <h3>New email is: {{ newEmail }}</h3>
    <form v-on:submit="pushItem">
      <input v-model="newEmail" placeholder="Enter email"/>
      <button type="submit">Add</button>
    </form>
  </div>
</template>

<style scoped>
.emails {
  margin: 20px;
}

h3 {
  font-size: 1.2rem;
}
</style>
