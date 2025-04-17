<template>
  <v-app>
    <v-main>
      <Carousel>
        <div style="background: #fce4ec; display: flex; align-items: center; justify-content: center;">
          <h2>Первый слайд — текст</h2>
        </div>

        <div style="background: #e3f2fd; display: flex; align-items: center; justify-content: center;">
          <img src="https://via.placeholder.com/300x200" alt="Изображение">
        </div>

        <div style="background: #f3e5f5; display: flex; align-items: center; justify-content: center;">
          <MyForm />
        </div>

        <div style="background: #e8f5e9; display: flex; align-items: center; justify-content: center;">
          <iframe
            width="300"
            height="200"
            src="https://www.youtube.com/embed/dQw4w9WgXcQ"
            title="YouTube video"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      </Carousel>
    </v-main>
  </v-app>
</template>

<script setup>
import Carousel from './components/Carousel.vue'
import MyForm from './components/MyForm.vue'

</script>