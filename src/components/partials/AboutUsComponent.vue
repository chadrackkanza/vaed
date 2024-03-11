<template>
  <div>
    <div class="bg-white px-6 sm:pb-24 lg:px-8">
      <div class="mx-auto max-w-5xl text-center">
        <p class="text-base font-semibold leading-7 text-red-600">A propos de nous</p>
        <h2 class="mt-2 text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl">
          Nous sommes une entreprise axée sur l'art graphique 🎨 et le marketing digital 📣
        </h2>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          Nos services diversifiés vous offrent de la valeur à tous les niveaux
        </p>
      </div>
    </div>
    <div
      class="grid grid-cols-1 gap-x-5 gap-y-12 sm:grid-cols-4 justify-items-center container mx-auto px-4"
    >
      <cardComponent
        :image-url="card.imageUrl"
        :titre="card.title"
        :description="card.description"
        v-for="(card, index) in cards"
        :key="index"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import CardComponent from '../cardComponent.vue'
import UiUx from '@/assets/images/ui-ux.png'
import PenTool from '@/assets/images/pen-tool.png'
import DigitalMarketing from '@/assets/images/digital-marketing.png'
import CommunityManagement from '@/assets/images/viral-marketing.png'

const cards = ref([
  {
    title: 'Design graphique',
    imageUrl: PenTool,
    description: 'Des affiches, des logos très belles et modernes'
  },
  {
    title: 'Web Design',
    imageUrl: UiUx,
    description: 'Des affiches, des logos très belles et modernes'
  },
  {
    title: 'Marketing digital',
    imageUrl: DigitalMarketing,
    description: 'Des affiches, des logos très belles et modernes'
  },
  {
    title: 'Community management',
    imageUrl: CommunityManagement,
    description: 'Des affiches, des logos très belles et modernes'
  }
])
</script>
