<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">{{ message }}</v-col>
    </v-row>
  </v-container>
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
  data: () => ({})
})
</script>
