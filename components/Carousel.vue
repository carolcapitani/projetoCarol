<template>
    <div class="relative">
      <div class="overflow-hidden relative" :style="{ height: carouselHeight + 'px' }">
        <div
          class="flex transition-transform duration-500 ease-in-out"
          :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
        >
          <img
            v-for="(image, index) in images"
            :key="index"
            :src="image.src"
            :alt="image.alt"
            class="w-64 h-64 object-cover rounded-lg mx-2" <!-- Ajustado para um tamanho fixo -->
        </div>
      </div>
      <div class="absolute top-1/2 right-0 transform -translate-y-1/2 text-white">
        <button
          class="bg-black bg-opacity-50 px-3 py-1 rounded-l-full"
          @click="nextSlide"
        >
          &#10095;
        </button>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  // Lista de imagens
  const images = ref([
    { src: '/images/gato1.jpg', alt: 'Imagem 1' },
    { src: '/images/gato2.jpg', alt: 'Imagem 2' },
    { src: '/images/gato3.jpg', alt: 'Imagem 3' },
    { src: '/images/gato4.jpg', alt: 'Imagem 4' },
    { src: '/images/gato6.jpg', alt: 'Imagem 6' },
    { src: '/images/gato7.jpg', alt: 'Imagem 7' },
    { src: '/images/gato8.jpg', alt: 'Imagem 8' },
    { src: '/images/gato9.jpg', alt: 'Imagem 9' },
    { src: '/images/gato10.jpg', alt: 'Imagem 10' },
    { src: '/images/gato11.jpg', alt: 'Imagem 11' },
    { src: '/images/gato12.jpg', alt: 'Imagem 12' },

  ]);
  
  const currentIndex = ref(0);
  const carouselHeight = ref(250); // altura do carrossel
  
  // Função para avançar para a próxima imagem
  const nextSlide = () => {
    if (currentIndex.value < images.value.length - 10) {
      currentIndex.value++;
    } else {
      currentIndex.value = 0; // Volta para a primeira imagem quando chega na última
    }
  };
  
  // Função para retroceder para a imagem anterior
  const prevSlide = () => {
    if (currentIndex.value > 0) {
      currentIndex.value--;
    } else {
      currentIndex.value = images.value.length - 1; // Vai para a última imagem
    }
  };
  
  // Função para ajustar o tamanho do carrossel conforme a tela
  onMounted(() => {
    window.addEventListener('resize', () => {
      carouselHeight.value = window.innerWidth / 10; // Ajuste a altura conforme desejado
    });
  
    // Avança automaticamente a cada 5 segundos
    const autoSlide = setInterval(() => {
      nextSlide();
    }, 4000);
  
    // Limpa o intervalo quando o componente for destruído
    onUnmounted(() => {
      clearInterval(autoSlide);
    });
  });
  </script>
  
  <style scoped>
  /* Estilo opcional para a transição */
  img {
    transition: transform 0.5s ease;
  }
  </style>
  