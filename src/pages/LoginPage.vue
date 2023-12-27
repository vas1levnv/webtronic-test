<template>
  <q-form
    ref="myForm"
    @submit="onSubmit"
    class="q-gutter-md"
  >
    <h5 class="text-center">Sign in</h5>

    <q-input
      outlined
      :dense="dense"
      v-model="email"
      placeholder="Email"
      :rules="[ val => val && val === 'admin' || 'Please type \'admin\' in field']"
    />

    <q-input
      outlined
      :dense="dense"
      type="password"
      v-model="password"
      placeholder="Password"
      :rules="[ val => val && val === 'admin' || 'Please type \'admin\' in field']"
    />

    <q-checkbox v-model="rememberMe" label="Remember me"/>
    <div>
      <q-btn label="Log in" style="width: 100%" type="submit" color="primary"/>
    </div>
    <div class="flex justify-between">
      <span>forgot your password</span>
      <span>create an account</span>
    </div>
  </q-form>
</template>

<script setup>

import {ref} from "vue";
import {useRouter} from "vue-router";

const myForm = ref(null)
const email = ref(null)
const password = ref(null)
const rememberMe = ref(null)
const dense = ref(false)
const router = useRouter()

const onSubmit = () => {
  router.push({path: '/'})
}

</script>

