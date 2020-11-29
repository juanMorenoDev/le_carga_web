<template>
  <v-form v-model="valid">
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            label="Nombre Completo"
            required
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="lastname"
            :rules="nameRules"
            label="Numero de telefono"
            required
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
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
    nameRules: [(v: string) => !!v || 'Campo requerido'],
    email: '',
    emailRules: [
      (v: string) => !!v || 'Campo requerido',
      (v: string) => /.+@.+/.test(v) || 'E-mail must be valid'
    ]
  })
})
</script>
