<template>
  <v-list nav dense>
    <v-list-item-group v-model="group">
      <v-list-item>
        <v-list-item-title>
          <v-btn outline color="primary" width="100%">Para conductores</v-btn>
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <v-btn outline color="primary" width="100%"
            >Para dueños de carro</v-btn
          >
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <v-btn outline color="primary" width="100%"
            >Para dueños de carga</v-btn
          >
        </v-list-item-title>
      </v-list-item>
      <v-list-item>
        <v-list-item-title>
          <v-btn outline color="primary" width="100%">Contactanos!</v-btn>
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
