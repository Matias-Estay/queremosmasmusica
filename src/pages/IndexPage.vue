<template>
  <q-tab-panels v-model="tab_mutation" animated>
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
import { computed, defineComponent} from 'vue'
import InicioTab from '../components/InicioTab.vue'
import AcademiaTab from '../components/AcademiaTab.vue'
import EstudioTab from '../components/EstudioTab.vue'
import ContactoTab from '../components/ContactoTab.vue'
export default defineComponent({
  name: 'IndexPage',
  props:{
    tab:{}
  },
  components: {
    InicioTab,
    AcademiaTab,
    EstudioTab,
    ContactoTab
  },
  setup(props){
    return{
      tab_mutation:computed(()=>{return props.tab})
    }

  }
})
</script>
