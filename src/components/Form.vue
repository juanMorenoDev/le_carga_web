<template>
  <v-form v-model="valid">
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            label="Nombre Completo"
            outlined
            solo
            filled
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="lastname"
            :rules="nameRules"
            label="Numero de telefono"
            required
            outlined
            solo
            filled
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
            outlined
            solo
            filled
          ></v-text-field>
        </v-col>
        <v-col cols="4" md="2">
          <v-select
            v-model="idType"
            :items="idTypeItems"
            label="Tipo de documento"
            required
            solo
            outlined
            filled
          ></v-select>
        </v-col>
        <v-col cols="8" md="4">
          <v-text-field
            v-model.number="idNumber"
            :rules="numberRules"
            label="Numero"
            required
            outlined
            solo
            filled
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="12">
          <div>
            Por favor seleccione la ciudad o ciudades en las que opera
            principalmente, escriba tantas como quiera separados por coma o la
            tecla enter
          </div>
          <v-combobox
            v-model="cities"
            hide-selected
            :items="initialCities"
            label="Ciudades donde opera"
            multiple
            outlined
            filled
            solo
            chips
            deletable-chips
            :delimiters="[',']"
          />
        </v-col>
        <v-col cols="12" md="12">
          <div>
            Por favor seleccione el tipo o tipos de carro que posee, escriba
            tantos como quiera separados por coma o la tecla enter
          </div>
          <v-combobox
            v-model="carTypes"
            hide-selected
            :items="initialCarTypes"
            label="Typos de carro que posee"
            multiple
            outlined
            filled
            solo
            chips
            deletable-chips
            :delimiters="[',']"
          />
        </v-col>
        <v-col>
          <v-btn
            color="primary"
            exact-active-class="class"
            to="/"
            type="submit"
          >
            Registrar
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'HelloWorld',
  props: {
    message: {
      type: String
    }
  },
  data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    carType: '',
    nameRules: [(v: string) => !!v || 'Campo requerido'],
    numberRules: [
      (v: number) => !!v || 'Campo requerido',
      (v: number) => typeof v === 'number' || 'Debe ser un numero'
    ],
    email: '',
    emailRules: [
      (v: string) => !!v || 'Campo requerido',
      (v: string) => /.+@.+/.test(v) || 'E-mail debe ser valido'
    ],
    idTypeItems: ['CC', 'NIT'],
    initialCarTypes: ['Turbo', 'DobleTroque', 'Sencillo'],
    initialCities: [
      'Ibague',
      'Medellin',
      'Bogota',
      'Barranquilla',
      'Villavicencio',
      'Santa Marta'
    ],
    cities: [],
    carTypes: [],
    idType: '',
    idNumber: null
  })
})
</script>
