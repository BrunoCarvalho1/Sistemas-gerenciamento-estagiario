<template>
  <q-page>
    <div class="row">
      <div class="col-12">
        <q-form style="margin: 50px;" class="row justify-center q-gutter-y-sm q-mx-md">
        <q-img
        src="../assets/logopmvc.png"
        style="width: 400px;"
        />
        <p class="col-12 text-h5 text-center"> EstagiHub </p>
        <div class="col-sm-6 col-md-8 col-lg-10 q-gutter-y-md">
          <q-input
          label="Email"
          v-model="form.email"
          outlined
          lazy-rules
          />
          <q-input
          label="Password"
          v-model="form.password"
          outlined
          lazy-rules
          />

          <div class="full-width q-pt-md">
            <q-btn
            label="Login"
            color="primary"
            class="full-width"
            outlined
            rounded
            type="submit"
            to="me"
          />
          </div>

        </div>

      </q-form>
      </div>
      <div class="col-6">
      </div>
  </div>
  </q-page>
</template>

<script lang="ts">

import { defineComponent } from 'vue'
// import useAuthUser from 'src/composables/useAuthUser'
// import { useRouter } from 'vue-router'
// import useNotify from 'src/composables/UseNotify'

export default defineComponent({
  name: 'PageLogin',
  data () {
    return {
      form: {
        email: '',
        password: ''
      }
    }
  }
})
</script>
