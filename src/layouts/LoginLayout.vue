<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <div class="form-wrapper">
        <router-view/>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>
import {defineComponent, ref} from 'vue'

export default defineComponent({
  name: 'MainLayout',

  setup() {

    return {}
  }
})
</script>

<style scoped lang="scss">
.form {
  &-wrapper {
    max-width: 400px;
    width: 100%;
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
}
</style>
