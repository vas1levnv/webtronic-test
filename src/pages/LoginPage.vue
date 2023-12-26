<template>
  <q-form
    @submit="onSubmit"
    class="flex column gap"
    style="gap: 0.5rem"
  >
    <h5 class="text-center">Sign in</h5>

    <q-input
      filled
      v-model="email"
      label="Your email *"
      lazy-rules
      :rules="[ val => val && val.length > 0 || 'Please type correct email']"
    />

    <q-input
      filled
      type="password"
      v-model="password"
      label="Your password *"
      lazy-rules
      :rules="[
          val => val && val.length > 6 || 'password must contain more than 6 characters'
        ]"
    />
    <q-checkbox v-model="rememberMe" label="Remember me"/>
    <q-btn label="Log in" @click="sendAuthForm" type="submit" color="primary"/>
    <div class="flex justify-between">
      <span>forgot your password</span>
      <span>create an account</span>
    </div>
  </q-form>
</template>

<script setup>

import {ref} from "vue";

const email = ref(null)
const password = ref(null)
const rememberMe = ref(null)

const sendAuthForm = (e) => {
  e.preventDefault()
  console.log(email.value, password.value, rememberMe.value)
}

</script>

