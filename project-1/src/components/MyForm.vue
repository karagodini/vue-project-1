<template>
  <v-form ref="formRef" @submit.prevent="submit" v-if="formVisible">
    <v-text-field
      v-model="name"
      label="Имя"
      :rules="[v => !!v || 'Введите имя']"
    />
    <v-text-field
      v-model="email"
      label="Email"
      :rules="[v => /.+@.+/.test(v) || 'Некорректный email']"
    />
    <v-btn type="submit" color="primary">Отправить</v-btn>
  </v-form>
</template>

<script>
export default {
  name: 'MyForm',
  data() {
    return {
      name: '',
      email: '',
      formVisible: true,
    }
  },
  methods: {
    submit() {
      this.$refs.formRef.validate().then(success => {
        if (success) {
          this.$emit('submit', { name: this.name, email: this.email })
        }
      })
    },
  },
}
</script>
