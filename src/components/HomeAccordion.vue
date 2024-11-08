<template>
  <div class="p-4 text-zinc-400">
    <div v-for="(item, index) in items" :key="index" class="py-2">
      <button
        type="button"
        class="flex items-center justify-between w-full p-4 text-left font-medium border-zinc-800"
        @click="toggle(index)"
        :aria-expanded="activeIndex === index ? 'true' : 'false'"
        :aria-controls="'accordion-body-' + index"
      >
        <span>{{ item.title }}</span>
        <svg
          :class="{'rotate-180': activeIndex === index}"
          class="w-5 h-5 transition-transform duration-300"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M19 9l-7 7-7-7"
          />
        </svg>
      </button>
      <div
        :id="'accordion-body-' + index"
        class="overflow-hidden transition-max-height duration-300 ease-in-out"
        :style="{
          maxHeight: activeIndex === index ? '1000px' : '0',
          opacity: activeIndex === index ? '1' : '0',
        }"
      >
        <div class="p-4 ">
          <p>{{ item.content }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface AccordionItem {
  title: string;
  content: string;
}

const items: AccordionItem[] = [
  {
    title: 'Diferenciação no Mercado',
    content:
      'Uma identidade visual forte destaca sua empresa entre a concorrência, tornando-a imediatamente reconhecível para os clientes. Isso cria uma vantagem competitiva, ajudando seu negócio a se destacar em um mercado saturado.',
  },
  {
    title: 'Apoio ao Crescimento do Negócio',
    content:
      'Com uma identidade visual sólida, sua empresa está preparada para crescer de forma escalável. Ela permite que você se expanda para novos mercados ou lance novos produtos sob uma imagem de marca unificada e bem estabelecida.',
  },
  {
    title: 'Credibilidade e Confiança',
    content:
      'Uma marca com uma identidade visual bem definida transmite profissionalismo e confiabilidade. Os clientes tendem a confiar mais em empresas que apresentam uma imagem coesa e visualmente atraente.',
  },
  {
    title: 'Potencializa Campanhas de Marketing',
    content:
      'Uma identidade visual coesa facilita a criação de campanhas de marketing mais eficazes e impactantes. Com elementos visuais consistentes, suas campanhas se tornam mais reconhecíveis e memoráveis, o que aumenta a eficácia das mensagens promocionais e melhora a conexão com o público-alvo.',
  },
];

const activeIndex = ref<number | null>(null);

const toggle = (index: number) => {
  activeIndex.value = activeIndex.value === index ? null : index;
};
</script>

<style scoped>

</style>
