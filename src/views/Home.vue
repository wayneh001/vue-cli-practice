<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="container">
      <div class="row">
        <div class="col-3 mx-auto mt-5">
          <Form></Form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Form from '@/components/Form.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Form
  }
}
</script>
