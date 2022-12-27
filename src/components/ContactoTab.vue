<template>
  <div class="row justify-center">
    <h3 class="q-mb-none">¿Tienes alguna duda?</h3>
  </div>
  <div class="row justify-center">
    <h6 class="q-mb-none q-mt-none">Contacta con nosotros</h6>
  </div>
  <div class="separator"/>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <q-input square filled v-model="nombre" label="Tu nombre" />
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {
    const nombre = ref('')
    return{
      nombre,
    }
  },
})
</script>
