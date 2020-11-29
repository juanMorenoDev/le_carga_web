<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
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
      </div>
    </v-app-bar>
    <v-main>
      <v-navigation-drawer v-model="drawer" class="drawer" temporary>
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
.drawer {
  position: absolute;
}
</style>
