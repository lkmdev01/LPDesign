<script setup lang="ts">
import { ref, onMounted, onUnmounted} from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

import HeaderNav from './components/HeaderNav.vue';
import MyHeader from './components/MyHeader.vue';
import MyServices from './components/MyServices.vue';
import MyPortfolio from './components/MyPortfolio.vue';
import MyTestimonials from './components/MyTestimonials.vue';
import MyFooter from './components/MyFooter.vue';
import HomeAccordion from './components/HomeAccordion.vue';

// Armazena o número de slides visíveis
const currentSlidesPerView = ref(calculateSlidesPerView());

// Calcula o número de slides visíveis com base na largura da tela
function calculateSlidesPerView() {
  const width = window.innerWidth;
  if (width < 600) return 1;
  if (width < 900) return 2;
  if (width < 1200) return 3;
  return 4; // Número máximo de slides visíveis para larguras maiores
}

// Atualiza o número de slides visíveis quando a janela é redimensionada
function updateSlidesPerView() {
  currentSlidesPerView.value = calculateSlidesPerView();
}

onMounted(() => {
  // Adiciona ouvinte de redimensionamento
  window.addEventListener('resize', updateSlidesPerView);
  // Atualiza o número de slides visíveis na montagem
  updateSlidesPerView();

  // Inicializa AOS
  AOS.init();
});

// Botão de voltar ao top

const showScrollTopButton = ref(false);

const checkScrollPosition = () => {
  if (window.scrollY > 200) { // Exibir o botão quando rolar mais de 200px
    showScrollTopButton.value = true;
  } else {
    showScrollTopButton.value = false;
  }
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(() => {
  window.addEventListener('scroll', checkScrollPosition);
});

onUnmounted(() => {
  window.removeEventListener('scroll', checkScrollPosition);
});


</script>

<template>
  <div>
    <HeaderNav></HeaderNav>
    <MyHeader></MyHeader>
    <section class="bg-zinc-950" data-aos="fade-up" data-aos-anchor-placement="top-center">
      <div class="my-container zinc-950 py-20 lg:pb-15">
        <h3 class="text-3xl font-bold text-zinc-100 pb-10">BENEFÍCIOS DE UMA IDENTIDADE VISUAL</h3>
        <HomeAccordion/>
      </div>
    </section>
    <MyServices data-aos="fade-up" data-aos-anchor-placement="top-center"></MyServices>
    <MyPortfolio data-aos="fade-up" data-aos-anchor-placement="top-center"></MyPortfolio>
    <MyTestimonials data-aos="fade-up" data-aos-anchor-placement="top-center"></MyTestimonials>
    <div class="fixed flex justify-center flex-col items-center bottom-4 right-4">
      <button v-if="showScrollTopButton" @click="scrollToTop" class="bg-zinc-800 w-12 h-12 text-white  mb-2 rounded-full shadow-lg hover:bg-zinc-700 hover:border-zinc-200">
        <i class="fa-solid fa-circle-arrow-up text-2xl"></i>
      </button>
      <button class="bg-green-700 w-12 h-12 text-white rounded-full shadow-lg hover:bg-green-600 hover:border-green-200">
        <a href="https://wa.me/5513981376072?text=Ol%C3%A1!%20Vim%20do%20site%20www.lkmdev.com%20%F0%9F%92%BB"><i class="fa-brands fa-whatsapp text-2xl text-white"></i></a>
      </button>
    </div>
    
    <MyFooter ></MyFooter>
  </div>
</template>

<style scoped>
.swiper-slide img {
    transition: filter 0.3s ease;
    filter: grayscale(1);
}
.swiper-slide:hover img {
    filter: grayscale(0);
}

.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}

.mySwiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
