<template>
  <div>
    <v-app-bar color="blue darken-4" height="70" />
    <ButtonsRow :buttons="buttons" fullWidth small class="drawer" />
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import ButtonsRow from '@/components/ButtonsRow.vue'
import buttons from '@/const/buttons'
export default Vue.extend({
  name: 'DrawerContent',
  components: {
    ButtonsRow
  },
  data: () => ({
    buttons
  })
})
</script>
<style scoped>
.drawer {
  margin: 10px auto;
  width: 90%;
}
</style>
