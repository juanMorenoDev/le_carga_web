<template>
  <v-app>
    <v-app-bar app color="blue darken-4" height="70" dark>
      <v-app-bar-nav-icon color="" @click.stop="drawer = !drawer" />
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
    <v-main class="">
      <v-navigation-drawer v-model="drawer" app fixed clipped temporary>
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
  background: white;
  color: #1976d2;
}
.bg_transparent {
  background: rgb(212, 212, 212, 0.6);
  color: #1976d2;
}
.v-application {
  font-family: 'Epilogue', sans-serif !important;
}
.title_font {
  font-family: 'Contrail One', cursive !important;
}
</style>
