<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/lecarga.svg" />
    <HelloWorld :message="message" />
    <Form />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src
import Form from '@/components/Form.vue' // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
    Form
  }
})
export default class Home extends Vue {
  message = 'Hello from lecarga'
}
</script>
