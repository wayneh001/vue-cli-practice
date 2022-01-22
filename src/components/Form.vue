<template>
  <Form @submit="onSubmit" v-slot="{ errors }">
    <div class="mb-3">
      <label for="email" class="form-label">Email</label>
      <Field
        id="email"
        name="email"
        type="email"
        class="form-control"
        placeholder="請輸入 Email"
        rules="email|required"
        :class="{ 'is-invalid': errors['email'] }"
        v-model="user.email"
      ></Field>
      <ErrorMessage name="email" class="invalid-feedback"></ErrorMessage>
    </div>

    <div class="mb-3">
      <label for="name" class="form-label">姓名</label>
      <Field
        id="name"
        name="姓名"
        type="text"
        class="form-control"
        placeholder="請輸入姓名"
        rules="required"
        :class="{ 'is-invalid': errors['姓名'] }"
        v-model="user.name"
      ></Field>
      <ErrorMessage name="姓名" class="invalid-feedback"></ErrorMessage>
    </div>

    <button class="btn btn-success" type="submit">Submit</button>
  </Form>
</template>

<script>
export default {
  data () {
    return {
      user: {
        email: '',
        name: ''
      }
    }
  },
  methods: {
    onSubmit () {
      console.log(this.user)
    }
  },
  created () {
    console.log(this)
  }
}
</script>
