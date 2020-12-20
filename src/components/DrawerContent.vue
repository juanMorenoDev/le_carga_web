<template>
  <div class="drawer">
    <ButtonsRow :buttons="buttons" fullWidth small />
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
  padding: 10px;
  width: 90%;
}
</style>
