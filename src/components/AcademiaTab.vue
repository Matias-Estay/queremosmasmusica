<template>
  <div class="row justify-center">
    <q-img src="/icons/queremosmasmusica-academia-logo.png" style="width:200px"></q-img>
  </div>
  <div class="row justify-center">
    <h3>Nuestra Academia de Música cuenta con modalidad online y presencial</h3>
  </div>
  <div class="row justify-center">
    <h3 class="q-mb-none">Nuestros Talleres</h3>
  </div>
  <div class="separator"/>
  <div class="row justify-center q-mt-md">
    <q-responsive :ratio="16/9" style="width: 1000px; max-width: 100%;">
      <q-carousel
        v-model="slide"
        :autoplay="4000"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        infinite
        control-color="white"
        navigation
        arrows
        class="text-white rounded-borders"
      >
        <q-carousel-slide name="taller1" img-src="/images/academia/taller1.jpg">
          <div class="absolute-center text-h3">
            Iniciación Musical
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller2" class="column no-wrap flex-center" img-src="/images/academia/taller2.jpg">
          <div class="absolute-center text-h3">
            Piano
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller3" class="column no-wrap flex-center" img-src="/images/academia/taller3.jpg">
          <div class="absolute-center text-h3">
            Guitarra
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller4" class="column no-wrap flex-center" img-src="/images/academia/taller4.jpg">
          <div class="absolute-center text-h3">
            Saxofón
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller5" class="column no-wrap flex-center" img-src="/images/academia/taller5.jpg">
          <div class="absolute-center text-h3">
            Ukelele
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller6" class="column no-wrap flex-center" img-src="/images/academia/taller6.jpg">
          <div class="absolute-center text-h3">
            Bajo
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller7" class="column no-wrap flex-center" img-src="/images/academia/taller7.jpg">
          <div class="absolute-center text-h3">
            Trompeta
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller8" class="column no-wrap flex-center" img-src="/images/academia/taller8.jpg">
          <div class="absolute-center text-h3">
            Trombón
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="taller9" class="column no-wrap flex-center" img-src="/images/academia/taller9.jpg">
          <div class="absolute-center text-h3">
            Bateria
          </div>
        </q-carousel-slide>
      </q-carousel>
    </q-responsive>
  </div>
  <div class="row justify-center">
    <h3 class="q-mb-none">Niveles según tu capacidad actual</h3>
  </div>
  <div class="separator"/>
  <div class="row justify-center q-gutter-xl q-mt-xs">
    <div class="col-xl-9">
      <q-card class="fit">
        <q-splitter
          v-model="splitterModel"
          before-class="h-40"
        >
          <template v-slot:before>
            <q-tabs
              v-model="nivel_tab"
              vertical
              class="text-teal"
            >
              <q-tab name="basico" icon="music_note" label="Nivel Elemental" style="color:#d6634f"/>
              <q-tab name="intermedio" icon="music_note music_note" label="Nivel Básico" style="color:#d6634f"/>
              <q-tab name="avanzado" icon="music_note music_note music_note" label="Nivel Intermedio" style="color:#d6634f"/>
            </q-tabs>
          </template>

          <template v-slot:after>
            <q-tab-panels
              v-model="nivel_tab"
              style="width:100%"
              animated
              vertical
              transition-prev="jump-up"
              transition-next="jump-up"
            >
              <q-tab-panel name="basico">
                <div class="text-h4 q-mb-md">¿Es tu primera vez con un instrumento musical?</div>
                <br/>
                Entonces, este nivel es para ti. No importa que edad tienes, si estas recién empezando necesitas empezar a desarrollar el pulso interno, habilidades y conceptos musicales básico. Desde como cuidar y mantener limpio tu instrumento hasta como tomarlo y ejecutar las primeras notas.
                <br/>
                <br/>
                Todos nuestros talleres están enfocados en desarrollar tus habilidades musicales de una forma didáctica y amigable. Las clases son completamente individuales y personalizadas. Siempre tratamos de poner todos los beneficios de la tecnología al servicio del aprendizaje.
                Desarrolla el oído musical, el lenguaje formal de la música y aprende tus canciones favoritas de la mano de repertorio que desarrolle las expectativas técnicas  para cada cada nivel. Tenemos experiencia desde los 5 años de edad.
            </q-tab-panel>

              <q-tab-panel name="intermedio">
                <div class="text-h4 q-mb-md">Si ya tocas otro instrumento o has tomado clases antes, este es tu nivel.</div>
                Comienza directamente a tocar tu nuevo instrumento. Dado que ya tienes conocimientos elementales como el pulso, las notas musicales, algunos acordes, lenguaje musical, como mantener tu instrumento en buenas condiciones y ejecutar algunas melodías.
                <br/>
                <br/>
                En este nivel comenzaras a ampliar tu lenguaje musical con nuevas armonías y repertorio mas avanzado. Comenzaremos a revisar repertorio mas competente que busque desarrollar la habilidad de tus manos y a realizar ejercicios que permitan desarrollar tu técnica de ejecución.
                <br/>
                <br/>
                Recuerda que todas nuestras clases son completamente individuales y personalizadas.
              </q-tab-panel>

              <q-tab-panel name="avanzado">
                <div class="text-h4 q-mb-md">En este nivel se busca ir desarrollando la música de forma mas profesional</div>
                En este nivel buscamos desarrollar las principales áreas de un interprete musical como son la interpretación y técnica. Aquí se busca inculcar el conocimiento formal del instrumento, ampliar su lenguaje musical buscando repertorio que nos generen nuevas metas y ampliar nuestro horizonte musical.
              </q-tab-panel>
            </q-tab-panels>
          </template>

        </q-splitter>
      </q-card>
    </div>
  </div>
  <div class="row justify-center">
    <h3 class="q-mb-none">Precios</h3>
  </div>
  <div class="separator"/>
  <div class="row justify-center q-mt-md q-gutter-lg">
    <div class="col-xl-3 col-lg-3 col-md-5 col-sm-12 col-xs-12">
      <q-card flat bordered class="my-card">
        <q-card-section>
          <div class="row justify-center">
            <q-avatar icon="home_work"  style="color:#d6634f;font-size:100px"/>
          </div>
          <div class="row" style="background-color:#d6634f; min-height: 50px;">
            <div class="col-12 text-center">
              <h3 class="q-mt-xs q-mb-xs" style="color:white">
                Plan a Distancia
              </h3>
            </div>
            <div class="col-12 text-center">
              <h6 class="q-mt-xs q-mb-xs" style="color:white">
                Zoom o Meet
              </h6>
            </div>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <div class="row justify-center">
            <h6 class="text-lined q-mt-none q-mb-none">
              $45.000
            </h6>
            <h6 class="q-mt-none q-mb-none text-positive">
              &nbsp;&nbsp; $37.000
            </h6>
            <h6 class="q-mt-none q-mb-none" style="font-weight: 250 !important">
              &nbsp; /4 clases
            </h6>
          </div>
        </q-card-section>
        <q-card-section>
          <q-list bordered separator>
            <q-item v-ripple>
              <q-item-section>
                <h6 class="text-center q-mt-none q-mb-none"><q-icon name="schedule" style="color:#d6634f"/>&nbsp;La duración de cada clases 60 minutos </h6>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="calendar_month" style="color:#d6634f"/>&nbsp;Una clase a la semana</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="person" style="color:#d6634f"/>&nbsp;Individuales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="done" style="color:#d6634f"/>&nbsp;Personalizada</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="cloud_download" style="color:#d6634f"/>&nbsp;Acceso a nuestra libreria de video Tutoriales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="description" style="color:#d6634f"/>&nbsp;Recibir material gráfico realizado a la medida para nuestros alumnos</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-xl-3 col-lg-3 col-md-5 col-sm-12 col-xs-12">
      <q-card flat bordered class="my-card">
        <q-card-section>
          <div class="row justify-center">
            <q-avatar icon="location_on"  style="color:#d6634f;font-size:100px"/>
          </div>
          <div class="row" style="background-color:#d6634f; min-height: 50px;">
            <div class="col-12 text-center">
              <h3 class="q-mt-xs q-mb-xs" style="color:white">
                Plan Presencial
              </h3>
            </div>
            <div class="col-12 text-center">
              <h6 class="q-mt-xs q-mb-xs" style="color:white">
                Santiago
              </h6>
            </div>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <div class="row justify-center">
            <h6 class="text-lined q-mt-none q-mb-none">
              $60.000
            </h6>
            <h6 class="q-mt-none q-mb-none text-positive">
              &nbsp;&nbsp; $50.000
            </h6>
            <h6 class="q-mt-none q-mb-none" style="font-weight: 250 !important">
              &nbsp; /4 clases
            </h6>
          </div>
        </q-card-section>
        <q-card-section>
          <q-list bordered separator>
            <q-item v-ripple>
              <q-item-section>
                <h6 class="text-center q-mt-none q-mb-none"><q-icon name="schedule" style="color:#d6634f"/>&nbsp;La duración de cada clases 60 minutos </h6>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="calendar_month" style="color:#d6634f"/>&nbsp;Una clase a la semana</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="person" style="color:#d6634f"/>&nbsp;Individuales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="done" style="color:#d6634f"/>&nbsp;Personalizada</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="cloud_download" style="color:#d6634f"/>&nbsp;Acceso a nuestra libreria de video Tutoriales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="description" style="color:#d6634f"/>&nbsp;Recibir material gráfico realizado a la medida para nuestros alumnos</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-xl-3 col-lg-3 col-md-5 col-sm-12 col-xs-12">
      <q-card flat bordered class="my-card">
        <q-card-section>
          <div class="row justify-center">
            <q-avatar icon="location_on"  style="color:#d6634f;font-size:100px"/>
          </div>
          <div class="row" style="background-color:#d6634f; min-height: 50px;">
            <div class="col-12 text-center">
              <h3 class="q-mt-xs q-mb-xs" style="color:white">
                Plan Presencial Intensivo
              </h3>
            </div>
            <div class="col-12 text-center">
              <h6 class="q-mt-xs q-mb-xs" style="color:white">
                Santiago
              </h6>
            </div>
          </div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <div class="row justify-center">
            <h6 class="text-lined q-mt-none q-mb-none">
              $90.000
            </h6>
            <h6 class="q-mt-none q-mb-none text-positive">
              &nbsp;&nbsp; $80.000
            </h6>
            <h6 class="q-mt-none q-mb-none" style="font-weight: 250 !important">
              &nbsp; /8 clases
            </h6>
          </div>
        </q-card-section>
        <q-card-section>
          <q-list bordered separator>
            <q-item v-ripple>
              <q-item-section>
                <h6 class="text-center q-mt-none q-mb-none"><q-icon name="schedule" style="color:#d6634f"/>&nbsp;La duración de cada clases 60 minutos </h6>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="calendar_month" style="color:#d6634f"/>&nbsp;dos clases a la semana</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="person" style="color:#d6634f"/>&nbsp;Individuales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="done" style="color:#d6634f"/>&nbsp;Personalizada</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="cloud_download" style="color:#d6634f"/>&nbsp;Acceso a nuestra libreria de video Tutoriales</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-item-section>
                <q-item-label>
                  <h6 class="text-center q-mt-none q-mb-none"><q-icon name="description" style="color:#d6634f"/>&nbsp;Recibir material gráfico realizado a la medida para nuestros alumnos</h6>
                </q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-card-section>
      </q-card>
    </div>
  </div>
  <div class="row justify-center">
    <h3 class="q-mb-none">Ubicación</h3>
  </div>
  <div class="separator"/>
  <div class="row justify-center q-mt-lg q-mb-lg mapouter">
    <div class="col-xl-6 gmap_canvas">
      <iframe class="gmap_iframe" width="100%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://maps.google.com/maps?width=350&amp;height=350&amp;hl=en&amp;q=mall plaza egaña&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed">
      </iframe>
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name:'AcademiaTab',
  setup() {
    const nivel_tab = ref('basico')
    return{
      nivel_tab,
      splitterModel: ref(20),
      slide:ref('taller1')
    }
  },
})
</script>

