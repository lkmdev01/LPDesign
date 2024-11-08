<script setup lang="ts">


</script>

<template>
  <div class="bg-zinc-950" id="servicos">
    <div class="my-container mx-auto md:text-left backline py-5 lg:py-28">
      <h2 class="text-purple-500 text-sm">SERVIÇOS</h2>
      <h3 class="text-4xl font-bold text-white">Superando as expectativas</h3>
      <p class="text-white mt-2 mb-10">Transformamos ideias em identidades visuais que destacam sua marca e cativam o público.</p>
      <div class="groupcard grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 text-left">
        <div class="card border border-purple-700 rounded-xl p-6 bg-zinc-925 hover:bg-zinc-900 transition duration-300">
          <div class="flex justify-start">
            <img src="/redessociais.png" alt="Logo" class="ml-0 w-24 bg-zinc-900 hover:border hover:border-zinc-600 p-3 rounded-md">
          </div>
          <h4 class="text-lg font-semibold text-white mt-4">Artes para Social Media</h4>
          <p class="text-sm text-gray-400 mt-2">Desenvolvemos artes visuais atraentes para suas redes sociais, focadas em aumentar o engajamento e destacar sua marca no ambiente digital.</p>
          <div class="buttom flex justify-start">
            <a href="https://wa.me/5513981376072?text=Ol%C3%A1!%20Vim%20pelo%20site%20lkmdev.com%20e%20me%20interessei%20pelo%20servi%C3%A7o%20de%20Software%20Sob%20Demanda." class="border border-zinc-700 py-4 px-6 mt-5 rounded-lg text-white hover:bg-zinc-600 hover:text-purple-500"><i class="fa-solid fa-arrow-right text-xl"></i></a>
          </div>
        </div>
        <div class="card border border-purple-700 rounded-xl p-6 bg-zinc-925 hover:bg-zinc-900 transition duration-300">
          <div class="flex justify-start">
            <img src="/campanhas.png" alt="Logo" class="ml-0 w-24 bg-zinc-900 hover:border hover:border-zinc-600 p-3 rounded-md">
          </div>
          <h4 class="text-lg font-semibold text-white mt-4">Design de Campanhas</h4>
          <p class="text-sm text-gray-400 mt-2">Criamos peças visuais estratégicas para campanhas publicitárias, capturando a atenção do público e maximizando o impacto das suas mensagens.</p>
          <div class="buttom flex justify-start">
            <a href="https://wa.me/5513981376072?text=Ol%C3%A1!%20Vim%20pelo%20site%20lkmdev.com%20e%20me%20interessei%20pelo%20servi%C3%A7o%20de%20Landing%20Page." class="border border-zinc-700 py-4 px-6 mt-5 rounded-lg text-white hover:bg-zinc-600 hover:text-purple-500"><i class="fa-solid fa-arrow-right text-xl"></i></a>
          </div>
        </div>
        <div class="card border border-purple-700 rounded-xl p-6 bg-zinc-925 hover:bg-zinc-900 transition duration-300">
          <div class="flex justify-start">
            <img src="/logotipo.png" alt="Logo" class="ml-0 w-24 bg-zinc-900 hover:border hover:border-zinc-600 p-3 rounded-md">
          </div>
          <h4 class="text-lg font-semibold text-white mt-4">Criação de Logotipos</h4> 
          <p class="text-sm text-gray-400 mt-2">Projetamos logotipos únicos que representam a essência da sua marca, criando uma identidade visual forte e memorável.</p>
          <div class="buttom flex justify-start">
            <a href="https://wa.me/5513981376072?text=Ol%C3%A1!%20Vim%20pelo%20site%20lkmdev.com%20e%20me%20interessei%20pelo%20servi%C3%A7o%20de%20E-commerce." class="border border-zinc-700 py-4 px-6 mt-5 rounded-lg text-white hover:bg-zinc-600 hover:text-purple-500"><i class="fa-solid fa-arrow-right text-xl"></i></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.img img {
  filter: grayscale(1);
  transition: filter 0.3s ease;
}

.card:hover .img img {
  filter: grayscale(0);
}
</style>
