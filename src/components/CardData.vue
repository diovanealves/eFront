<script lang="ts">
import { PhClock, PhDiscordLogo, PhLightning, PhTarget } from '@phosphor-icons/vue'
import { ref } from 'vue'
import CardComponent from './CardComponent.vue'

const cardDataList = ref([
  {
    icon: PhClock,
    title: 'Reembolso',
    description:
      'Se por algum motivo você não gostar dos materiais você pode reembolsar sem taxa e perguntas.'
  },
  {
    icon: PhLightning,
    title: 'Vitalício',
    description:
      'Você tem acesso a todas as atualizações e para sempre. Basta acessar a plataforma da Hotmart.'
  },
  {
    icon: PhDiscordLogo,
    title: 'Comunidade',
    description:
      'Você terá acesso a comunidade exclusiva do Discord, onde utilizamos para resolver dúvidas.'
  },
  {
    icon: PhTarget,
    title: 'Notion',
    description:
      'Através do Notion você tem acesso aos materiais para realizar os estudos sobre frontend e design.'
  }
])

export default {
  components: { CardComponent },
  setup() {
    return { cardDataList }
  }
}
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-14 mt-16 mx-auto">
    <CardComponent
      v-for="data in cardDataList"
      :key="data.title"
      :icon="data.icon"
      :title="data.title"
      :description="data.description"
    />
  </div>
</template>
