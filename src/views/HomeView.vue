<script lang="ts">
import CardData from '@/components/CardData.vue'
import PriceComponent from '@/components/PriceComponent.vue'
import logo from '../assets/logoeFront.png'

export default {
  data() {
    return {
      logo
    }
  },
  components: { PriceComponent, CardData }
}
</script>

<template>
  <div class="flex flex-col max-w-7xl mx-auto px-7">
    <div class="mx-auto p-5">
      <h1>Aproveite os últimos dias de promoção</h1>
    </div>

    <div class="flex items-center justify-between mt-4">
      <img :src="logo" alt="Logo da eFront" class="w-7 h-8" />

      <RouterLink to="#">
        <button>Login</button>
      </RouterLink>
    </div>

    <div class="md:w-3/5 mx-auto grid place-items-center lg:grid-cols-2 lg:w-full gap-10 mt-10">
      <div class="space-y-4">
        <h1 class="text-3xl md:text-5xl">
          Comece a estudar <span class="text-[#899BFF]">frontend</span> do zero com uma linguagem
          simples
        </h1>
        <p class="text-[#CCCCCC] text-base md:text-lg">
          Trabalhe de casa, usando as tecnologias mais requisitados do mercado frontend.
        </p>
      </div>

      <PriceComponent />
    </div>
    <CardData />
  </div>
</template>
