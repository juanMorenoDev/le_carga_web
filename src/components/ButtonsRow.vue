<template>
  <v-row class="buttons-row">
    <v-btn
      v-for="(button, index) in buttons"
      :key="index"
      color="primary"
      class="ma-1"
      :width="width"
      @click="toRegistration(button.pathName)"
    >
      <v-col align-self="start">{{ button.label }}</v-col>
      <v-icon right>{{ button.icon }}</v-icon>
    </v-btn>
  </v-row>
</template>

<script lang="ts">
import Vue from 'vue'
import { ButtonProps } from '@/interfaces/ButtonProps'

export default Vue.extend({
  name: 'ButtonsRow',
  props: {
    buttons: {
      type: Array as () => ButtonProps[]
    }
  },
  methods: {
    toRegistration(path: string) {
      this.$router.push(path)
    }
  },
  computed: {
    width(): string {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return '100%'
        case 'sm':
          return '100%'
        default:
          return 'auto'
      }
    }
  }
})
</script>
