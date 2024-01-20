<script lang="ts">
import PriceComponent from '@/components/PriceComponent.vue'
import logo from '../assets/logoeFront.png'

export default {
  data() {
    return {
      logo
    }
  },
  components: { PriceComponent }
}
</script>

<template>
  <div class="flex flex-col max-w-7xl mx-auto px-7">
    <div class="mx-auto p-5">
      <h1>Aproveite os últimos dias de promoção</h1>
    </div>

    <div class="flex items-center justify-between mt-4">
      <img :src="logo" alt="Logo da eFront" class="w-7 h-8" />

      <RouterLink to="/login">
        <button>Login</button>
      </RouterLink>
    </div>

    <div class="grid grid-row-2 md:grid-cols-2 items-center place-items-end mt-16 gap-10">
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
  </div>
</template>
