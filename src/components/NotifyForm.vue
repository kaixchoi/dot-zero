<script setup>
import { ref } from 'vue'

const email = ref('')
const submitted = ref(false)

function submitForm() {
  if (!email.value) return
  submitted.value = true
}
</script>

<template>
  <div class="notify-form-wrap">
    <form v-if="!submitted" class="notify-form" @submit.prevent="submitForm">
      <label class="sr-only" for="email">Email address</label>
      <input id="email" v-model="email" type="email" placeholder="Your email address" required />
      <button type="submit">Keep me posted <span aria-hidden="true">&#8599;</span></button>
    </form>
    <p v-else class="form-success" role="status">You’re on the list. See you at zero.</p>
    <p class="form-note">No noise. Just the launch note.</p>
  </div>
</template>
