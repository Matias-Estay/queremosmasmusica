<template>
  <q-carousel
      arrows
      animated
      control-color="white"
      v-model="slide"
      height="400px"
    >
    <q-carousel-slide class="column no-wrap" name="first">
      <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide1.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide1-1.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide1-2.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide1-3.jpg" />
      </div>
      <div class="absolute-bottom custom-caption">
        <div class="text-h3">Home Estudio Santiago</div>
        <div class="text-subtitle1">Trabajos de Producción Musical</div>
      </div>
    </q-carousel-slide>
    <q-carousel-slide class="column no-wrap" name="second">
      <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide2.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide2-1.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide2-2.jpg" />
        <q-img class="rounded-borders col-xl-3 col-xs-12 full-height" src="/images/slide2-3.jpg" />
      </div>
      <div class="absolute-bottom custom-caption">
        <div class="text-h3">Academia QM</div>
        <div class="text-subtitle1">Área enfocada en la capacitación de nuevos músicos con clases particulares de instrumentos musicales</div>
      </div>
    </q-carousel-slide>
    <q-carousel-slide name="third" img-src="https://cdn.quasar.dev/img/parallax2.jpg">
      <div class="absolute-bottom custom-caption">
        <div class="text-h3">Third stop</div>
        <div class="text-subtitle1">Famous Bridge</div>
      </div>
    </q-carousel-slide>
  </q-carousel>
  <div class="row justify-center">
    <h3 class="nunito q-mb-xs text-center">
      Somos la Productora musical QM
    </h3>
  </div>
  <div class="row justify-center">
    <h3 class="q-mt-xs q-mb-xs text-center nunito" style="color: #FF7C7C">
      "Queremos más música"
    </h3>
  </div>
  <q-separator/>
</template>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'InicioTab',
  setup(){
    const slide = ref('first')
    const texto_dinamico = ref('¿Te interesarían Clases Musicales?')
    return{
      texto_dinamico,
      slide
    }
  }
})

</script>
