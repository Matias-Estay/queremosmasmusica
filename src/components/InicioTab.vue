<template>
  <q-carousel
      arrows
      animated
      control-color="white"
      v-model="slide"
      height="400px"
    >
    <q-carousel-slide class="column" name="first">
      <div class="row fit no-wrap items-center q-col-gutter " style="overflow-y: hidden;">
          <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide2.jpg" />
          <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide2-1.jpg" />
          <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide2-2.jpg" />
          <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide2-3.jpg" />
      </div>
      <div class="absolute-bottom custom-caption">
        <div class="text-h3">Academia QM</div>
        <div class="text-subtitle1">Área enfocada en la capacitación de nuevos músicos con clases particulares de instrumentos musicales</div>
      </div>
    </q-carousel-slide>
    <q-carousel-slide class="column" name="second">
      <div class="row fit no-wrap items-center q-col-gutter" style="overflow-y: hidden;">
        <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide1.jpg" />
        <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide1-1.jpg" />
        <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide1-2.jpg" />
        <q-img class="rounded-borders col-xl-3 col-lg-6 col-md-6 col-md-6 col-xs-12" src="/images/slide1-3.jpg" />
      </div>
      <div class="absolute-bottom custom-caption">
        <div class="text-h3">Home Studio Santiago</div>
        <div class="text-subtitle1">Trabajos de Producción Musical</div>
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
  <div class="separator"/>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-10 col-lg-10 col-md-10 col-sm-12 col-xs-12">
      <q-card bordered class=" my-card shadow-4">
        <q-card-section>
          <div class="text-h6">Quienes Somos</div>
        </q-card-section>
        <q-separator/>
        <q-card-section>
          <div class="row justify-center">
            <div class="col-xl-11">
              Felipe Chávez y Elías Irigoyen son Titulados de la Escuela Moderna de Música y Danza, como Compositores y Arregladores profesionales.Ademas tienen estudios formales de Licenciaturas en Artes musicales y de bandas orquestales, también a su vez, de Producción Musical moderna popular.
              Las herramientas que les han entregados estas distintas instituciones van con el desarrollo de: teoría musical, armonía popular, composición musical popular, arreglos musicales, contrapunto, orquestación, producción musical, piano funcional, historia de la música, dirección coral, entre otras cosas.
            </div>
        </div>
        </q-card-section>
      </q-card>
    </div>
  </div>
  <div class="row justify-center q-mt-lg q-gutter-md">
    <div class="col-xl-10 col-lg-10 col-md-10 col-sm-12 col-xs-12">
      <div class="row justify-center">
        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-xs-12 text-center">
          <div class="video-responsive">
          <iframe src="https://www.youtube.com/embed/qs6U3HKopcU?ecver=1&amp;iv_load_policy=1&amp;yt:stretch=16:9&amp;autohide=1&amp;color=red" width="560" height="315" allowtransparency="true" frameborder="0">
          </iframe>
          </div>
        </div>
        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-xs-12 text-center">
          <div class="video-responsive">
            <iframe src="https://www.youtube.com/embed/tje_l-tAtwI?ecver=1&amp;iv_load_policy=1&amp;yt:stretch=16:9&amp;autohide=1&amp;color=red" allowtransparency="true" frameborder="0">
            </iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
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
