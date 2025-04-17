<template>
  <v-app>
    <v-main>
      <Carousel>
        <div style="background: #fce4ec; display: flex; align-items: center; justify-content: center;">
          <h2>Текст</h2>
        </div>

        <div style="background: #e3f2fd; display: flex; align-items: center; justify-content: center;">
          <img src="@/assets/logo.png" alt="Изображение">
        </div>

        <div style="background: #f3e5f5; display: flex; align-items: center; justify-content: center;">
          <MyForm />
        </div>

        <div style="background: #e8f5e9; display: flex; align-items: center; justify-content: center;">
          <iframe width="100%" height="100%" src="https://rutube.ru/play/embed/9f25cf38c11555eb0c18a7496a0d0055/" frameBorder="0" allow="clipboard-write; autoplay" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
        </div>
      </Carousel>
    </v-main>
  </v-app>
</template>

<script setup>
import Carousel from './components/Carousel.vue'
import MyForm from './components/MyForm.vue'

</script>