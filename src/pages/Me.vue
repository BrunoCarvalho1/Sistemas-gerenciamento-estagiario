<template>
  <q-page padding>
    <div class="row q-col-gutter-md">
      <div class="col-md-3 col-xs-12 col-sm-6 ">
        <q-card class="q-pa-ms" style="background: radial-gradient(circle, #08ce82 0%, #018866 100%)">
          <q-card-section class="q-ma-xl">
            <div class="text-h6">Total de estágiarios: </div>
          </q-card-section>
        </q-card>
        <q-card class="q-pa-ms" style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)">
          <q-card-section class="q-ma-xl">
            <div class="text-h6">Estágiarios de férias: </div>
          </q-card-section>
        </q-card>
        <q-card class="q-pa-ms" style="background: radial-gradient(circle, #eb7531 0%, #e06d0e 100%)">
          <q-card-section class="q-ma-xl">
            <div class="text-h6">Finalizando contratos: </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageMe'
})
</script>
