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
    <q-tab-panel name="Inicio">
      <InicioTab></InicioTab>
    </q-tab-panel>

    <q-tab-panel name="Academia">
      <AcademiaTab></AcademiaTab>
    </q-tab-panel>

    <q-tab-panel name="Home Estudio">
      <EstudioTab></EstudioTab>
    </q-tab-panel>

    <q-tab-panel name="Contacto">
      <ContactoTab></ContactoTab>
    </q-tab-panel>
  </q-tab-panels>

</template>

<script>
import { defineComponent, ref } from 'vue'
import InicioTab from '../components/InicioTab.vue'
import AcademiaTab from '../components/AcademiaTab.vue'
import EstudioTab from '../components/EstudioTab.vue'
import ContactoTab from '../components/ContactoTab.vue'
export default defineComponent({
  name: 'IndexPage',
  components: {
    InicioTab,
    AcademiaTab,
    EstudioTab,
    ContactoTab
  },
  setup(){
    const tab = ref('Inicio')
    return{
      tab,
    }
  }
})
</script>
