<template>
  <v-list nav dense>
    <v-list-item-group>
      <v-list-item>
        <v-list-item-title>
          <router-link to="/">
            <v-btn color="primary" width="100%" small>
              <v-col align-self="start"> Para conductores </v-col>
              <v-icon right>mdi-car-child-seat</v-icon>
            </v-btn></router-link
          >
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <router-link to="/about">
            <v-btn color="primary" width="100%" small>
              <v-col align-self="start"> Dueños de carro </v-col>
              <v-icon right>mdi-truck</v-icon>
            </v-btn>
          </router-link>
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <router-link to="/about">
            <v-btn color="primary" width="100%" small>
              <v-col align-self="start">Proveedores de carga</v-col>
              <v-icon right>mdi-package-down</v-icon>
            </v-btn>
          </router-link>
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <router-link to="/about">
            <v-btn color="primary" width="100%" small>
              <v-icon>mdi-whatsapp</v-icon> Contactanos!</v-btn
            >
          </router-link>
        </v-list-item-title>
      </v-list-item>
    </v-list-item-group>
  </v-list>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DrawerContent',
  data: () => ({})
})
</script>
