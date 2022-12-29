<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated reveal>
      <q-toolbar class="bg-black text-white">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
        <q-avatar>
          <img src="/icons/queremosmasmusica-logo.png">
        </q-avatar>
        <q-toolbar-title>
          Queremos más Música
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
    >
      <q-list>
        <q-item-label
          header
        >

        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container style="padding-top:50px !important;">
      <router-view />
    </q-page-container>
    <q-page-sticky position="top-right" :offset="[18, 55]">
      <q-btn
        :href="'https://api.whatsapp.com/send/?phone=56995987737&text=Hola%2Cnecesito+más+información%21&type=phone_number&app_absent=0'"
        style="background-color:#25d366;color:white;width: 50px;"
        size="20px"
        round
        icon="bi-whatsapp"
      />
    </q-page-sticky>
    <q-footer class="bg-grey-6 text-white absolute-bottom">
      <q-toolbar>
        <q-toolbar-title>
          <div class="text-center">Copyright © Queremos más música</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Academia YouTube',
    caption: '',
    icon: 'bi-youtube',
    link: 'https://www.youtube.com/channel/UC5HSowoiIvbq6xk1qgSwHVg/videos',
    color: 'red',
    classes: ''
  },
  {
    title: 'Academia Instagram',
    caption: '',
    icon: 'bi-instagram',
    link: 'https://www.instagram.com/academia_qm/',
    color: '',
    classes: 'insta'
  },
  {
    title: 'Academia Facebook',
    caption: '',
    icon: 'bi-facebook',
    link: 'https://www.facebook.com/Academiaqm?_rdc=1&_rdr',
    color: 'blue',
    classes: ''
  },
  {
    title: 'Home Estudio Youtube',
    caption: '',
    icon: 'bi-youtube',
    link: 'https://www.youtube.com/channel/UCxmQlYGIjctreNKN4wwJSAQ',
    color: 'red',
    classes: ''
  },
  {
    title: 'Home Estudio Instagram',
    caption: '',
    icon: 'bi-instagram',
    link: 'https://www.instagram.com/homeestudio_qm/',
    color: '',
    classes: 'insta'
  },
  {
    title: 'Home Estudio Facebook',
    caption: '',
    icon: 'bi-facebook',
    link: 'https://www.facebook.com/HomeEstudioQM?_rdc=1&_rdr',
    color: 'blue',
    classes: ''
  }
]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
