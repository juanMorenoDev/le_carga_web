<template>
  <v-row>
    <v-btn
      v-for="(button, index) in buttons"
      :key="index"
      color="blue darken-4"
      class="ma-1"
      :style="{ color: 'white' }"
      :width="width"
      :to="button.pathName"
      :small="small"
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
    },
    fullWidth: {
      type: Boolean
    },
    small: {
      type: Boolean
    }
  },
  computed: {
    width(): string {
      if (this.fullWidth) {
        return '100%'
      } else {
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
  }
})
</script>
