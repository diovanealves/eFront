<script setup lang="ts">
import { defineProps } from 'vue'

const { icon, title, description } = defineProps(['icon', 'title', 'description'])
</script>

<template>
  <div>
    <component :is="icon" class="text-4xl" />
    <h1 class="text-2xl font-medium mt-7 mb-4">{{ title }}</h1>
    <p>{{ description }}</p>
  </div>
</template>
