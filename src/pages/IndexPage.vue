<template>
  <q-tabs
    v-model="tab"
    inline-label
    class="bg-grey-3"
  >
    <q-tab name="Inicio" label="Inicio"/>
    <q-tab name="Academia" label="Academia" />
    <q-tab name="Home Estudio" label="Home Estudio" />
    <q-tab name="Contacto" icon="mail" label="Contacto" />
  </q-tabs>
  <q-tab-panels v-model="tab" animated>
    <q-tab-panel v-model="tab" name="Inicio">
      <InicioTab></InicioTab>
    </q-tab-panel>

    <q-tab-panel v-model="tab" name="Academia">
      <AcademiaTab></AcademiaTab>
    </q-tab-panel>

    <q-tab-panel v-model="tab" name="Home Estudio">
      <div class="text-h6">Movies</div>
      Lorem ipsum dolor sit amet consectetur adipisicing elit.
    </q-tab-panel>
    <q-tab-panel v-model="tab" name="Contacto">
      <div class="text-h6">Movies</div>
      Etesech
    </q-tab-panel>
  </q-tab-panels>

</template>

<script>
import { defineComponent, ref } from 'vue'
import InicioTab from '../components/InicioTab.vue'
import AcademiaTab from '../components/AcademiaTab.vue'
export default defineComponent({
  name: 'IndexPage',
  components: {
    InicioTab,
    AcademiaTab
  },
  setup(){
    const tab = ref('Inicio')
    return{
      tab,
    }
  }
})
</script>
