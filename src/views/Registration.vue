<template>
  <div class="position">
    <v-img src="@/assets/road.jpg" position="center">
      <div class="image_container">
        <Form />
      </div>
    </v-img>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Form from '@/components/Form.vue' // @ is an alias to /src

@Component({
  components: {
    Form
  }
})
export default class Registration extends Vue {
  message = 'Hello from lecarga'
}
</script>
<style scoped>
.image_container {
  padding-top: 5em;
  display: flex;
  flex-flow: column;
  height: 100vh;
  width: 100vw;
}
.position {
  position: fixed;
  top: 0;
  height: 100vh;
  width: 100vw;
}
</style>
