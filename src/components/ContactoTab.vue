<template>
  <div class="row justify-center">
    <h3 class="q-mb-none">¿Tienes alguna duda?</h3>
  </div>
  <div class="row justify-center">
    <h6 class="q-mb-none q-mt-none">Contacta con nosotros</h6>
  </div>
  <div class="separator"/>
  <q-form
      @submit="Enviar_Correo"
      class="q-gutter-md"
    >
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <q-input square filled v-model="nombre" label="Tu nombre" :rules="[ val => val!= '' || 'Este campo no puede estar vacío' ]" />
    </div>
  </div>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <q-input type="email" square filled v-model="email" label="Correo" :rules="[ val => val.includes('@') || 'Ingresa un correo válido con @' ]" />
    </div>
  </div>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <q-input square filled v-model="asunto" label="asunto" :rules="[ val => val!= '' || 'Este campo no puede estar vacío' ]"/>
    </div>
  </div>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <q-field ref="fieldRef" v-model="mensaje" label-slot borderless
      :rules="[ val => val!= '' || 'Este campo no puede estar vacío' ]" >
        <template #label>Mensaje</template>
        <template #control>
          <q-editor v-model="mensaje" min-height="5rem" class="q-mt-md full-width"
            :style="$refs.fieldRef && $refs.fieldRef.hasError ? 'border-color: #C10015' : ''"/>
        </template>
      </q-field>
    </div>
  </div>
  <div class="row justify-center q-mt-lg">
    <div class="col-xl-9">
      <vue-recaptcha @verify="verifyMethod" sitekey="6LfiYbAjAAAAAAf02Mxvf7lnyiOgYZ0R1XqP_Lq-"></vue-recaptcha>
    </div>
  </div>
  <div class="row justify-center">
    <div class="col-xl-9">
      <q-btn type="submit" class="float-right q-mt-md text-white" style="background-color: #d6634f;">
        <q-spinner-hourglass
          v-if="cargando==true"
          :disabled="cargando==true"
          color="white"
          size="1em"
        />
        Enviar Correo
      </q-btn>
    </div>
  </div>
  </q-form>
</template>
<script>
import { defineComponent, ref } from 'vue'
import { VueRecaptcha } from 'vue-recaptcha';
import { useQuasar } from 'quasar'
import axios from 'axios'
export default defineComponent({
  components:{
    VueRecaptcha
  },
  setup() {
    const $q = useQuasar();
    const nombre = ref('');
    const email = ref('');
    const asunto = ref('');
    const mensaje = ref('');
    const captcha_valido = ref('');
    const cargando = ref(false);

    const Enviar_Correo = ()=>{
      if(captcha_valido.value){
        cargando.value=true;
        axios.post('https://emailqueremosmusica.onrender.com/api/envio_email',{name:nombre.value, subject: asunto.value, body:mensaje.value, email:email.value}).then(result=>{
          if(result.data.message=='OK'){
            $q.notify({
              type: 'positive',
              message: 'Se ha enviado el correo correctamente.'
            })
            cargando.value=false;
          }else{
            $q.notify({
              type: 'negative',
              message: 'Se ha generado un problema al enviar el correo, por favor verificar la dirección.'
            })
            cargando.value=false;
          }
        })
      }
    };
    const verifyMethod = (event)=>{
      if(event){
        captcha_valido.value=event
      }
    }
    return{
      nombre,
      email,
      asunto,
      mensaje,
      cargando,
      captcha_valido,
      Enviar_Correo,
      verifyMethod
    }
  },
})
</script>
