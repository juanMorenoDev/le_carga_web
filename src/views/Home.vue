<template>
  <div class="color_blue">
    <v-parallax src="@/assets/truckside.jpg">
      <v-row>
        <v-col cols="12" md="6">
          <div class="card bg_blue">
            <div class="card_body">
              <div class="card_title title_font">
                ¡Bienvenido a Le Carga!
              </div>
              <div class="card_text">
                Logistica y estrategias de carga es una plataforma diseñada con
                el objetivo principal de crear enlaces basados en la confianza
                entre transportadores, propietarios de vehiculos de carga y
                empresas generadoras de carga
              </div>
              <br />
            </div>
          </div>
        </v-col>
        <v-col cols="12" m="4"></v-col>
      </v-row>
    </v-parallax>
    <div class="signup">
      <div class="card_body">
        <v-row>
          <v-col cols="12" md="3">
            <div class="text-center">
              <img class="image" src="@/assets/signup.svg" />
            </div>
          </v-col>
          <v-col cols="12" md="9">
            <div class="card_title title_font">¡Registrate!</div>
            <div class="card_text">
              ¿Estas involucrado en el area del transporte? ¿Eres un proveedor
              de carga que necesita contratar transporte recurrentemente?
              ¿Tienes un vehiculo de carga? ¿Eres un conductor de vehiculos de
              transporte de cualquier tipo?
            </div>
          </v-col>
        </v-row>
      </div>
    </div>
    <Form />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src
import Form from '@/components/Form.vue' // @ is an alias to /src
import DrawerContent from '@/components/DrawerContent.vue'

@Component({
  components: {
    HelloWorld,
    Form,
    DrawerContent
  }
})
export default class Home extends Vue {
  message = 'Hello from lecarga'
}
</script>
<style scoped>
.bold {
  font-weight: bold;
}
.image {
  margin-top: 20px;
  width: 400px;
}
.card {
  margin: 15px 20px;
  padding: 20px;
  /* border-radius: 25px; */
  box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);
}
.color_blue {
  color: #1976d2;
}
.card_body {
  display: flex;
  flex-flow: column;
}
.card_text {
  font-size: 1.5em;
  word-break: keep-all;
  text-align: left;
}
.background {
  position: fixed;
  bottom: 0;
  right: 0;
}
.card_title {
  font-size: 2.5em;
  font-weight: 400;
  margin: 0.2em 0;
}
.signup {
  margin: 40px 60px 40px 40px;
}
@media (max-width: 500px) {
  .card {
    margin: 10px 10px;
  }
  .card_title {
    font-size: 2em;
  }
  .card_text {
    font-size: 1.2em;
    text-align: left;
  }
  .image {
    width: 200px;
  }
}
</style>
