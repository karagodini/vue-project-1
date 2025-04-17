<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12">
        <div class="carousel-wrapper">
          <v-btn
            icon
            class="carousel-btn left"
            @click="prev"
            :disabled="currentIndex === 0"
          >
            <v-icon>mdi-chevron-left</v-icon>
          </v-btn>

          <div class="carousel-track">
            <div
              class="carousel-slide"
              :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
            >
              <slot />
            </div>
          </div>

          <v-btn
            icon
            class="carousel-btn right"
            @click="next"
            :disabled="currentIndex === total - 1"
          >
            <v-icon>mdi-chevron-right</v-icon>
          </v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const currentIndex = ref(0)
const total = ref(0)

onMounted(() => {
  const slotContent = document.querySelectorAll('.carousel-slide > *')
  total.value = slotContent.length
})

const next = () => {
  if (currentIndex.value < total.value - 1) {
    currentIndex.value++
  }
}

const prev = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--
  }
}
</script>

