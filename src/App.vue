<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <router-link to="/">
        <v-img
          alt="Le carga"
          contain
          min-width="100"
          src="./assets/lecarga-white.svg"
          width="100"
        />
      </router-link>
    </v-app-bar>
    <v-main class="bg_gray">
      <v-navigation-drawer v-model="drawer" absolute temporary>
        <DrawerContent />
      </v-navigation-drawer>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import DrawerContent from './components/DrawerContent.vue'

export default Vue.extend({
  name: 'App',

  components: {
    DrawerContent
  },

  data: () => ({
    drawer: false
  })
})
</script>
<style>
.bg_blue {
  background: #1976d2;
  color: white;
}
.bg_gray {
  background: lightgray;
  color: #1976d2;
}
.v-application {
  font-family: 'Epilogue', sans-serif !important;
}
</style>
