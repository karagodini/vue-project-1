<template>
  <form @submit.prevent="submit" ref="formRef" class="custom-form">
    <div class="form-group">
      <label for="name">Имя</label>
      <input
        id="name"
        v-model="name"
        type="text"
        required
        placeholder="Введите имя"
      />
    </div>

    <div class="form-group">
      <label for="email">Email</label>
      <input
        id="email"
        v-model="email"
        type="email"
        required
        placeholder="Введите email"
      />
    </div>

    <button type="submit">Отправить</button>
  </form>
</template>

<script>
export default {
  name: 'MyForm',
  data() {
    return {
      name: '',
      email: '',
    }
  },
  methods: {
    submit() {
      if (this.name && this.email && /.+@.+\..+/.test(this.email)) {
        this.$emit('submit', { name: this.name, email: this.email })
      } else {
        alert('Пожалуйста, заполните поля корректно.')
      }
    },
  },
}
</script>