<template>
  <div
    class="relative flex max-w-72 flex-col rounded-xl bg-white bg-clip-border text-gray-700 shadow-md"
  >
    <div
      class="relative mx-4 -mt-6 h-40 overflow-hidden rounded-xl bg-blue-gray-500 bg-clip-border text-white shadow-sm shadow-gray-500/40 bg-gradient-to-r from-red-600 to-red-500 flex justify-center items-center"
    >
      <img :src="props.imageUrl" alt="" class="h-32" />
    </div>
    <div class="p-6">
      <h5
        class="mb-2 block font-sans text-xl font-semibold leading-snug tracking-normal text-blue-gray-900 antialiased"
      >
        {{ props.titre }}
      </h5>
      <p class="block font-sans text-base font-light leading-relaxed text-inherit antialiased">
        {{ props.description }}
      </p>
    </div>
    <div class="p-6 pt-0">
      <button
        data-ripple-light="true"
        type="button"
        class="select-none rounded-lg bg-red-600 py-3 px-6 text-center align-middle font-sans text-xs font-bold capitalize text-white shadow-md shadow-blue-500/20 transition-all hover:shadow-lg hover:shadow-red-500/40 focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] active:shadow-none disabled:pointer-events-none disabled:opacity-50 disabled:shadow-none"
      >
        {{ props.textButton }}
      </button>
    </div>
  </div>
</template>

<script setup>
// const props = defineProps(['imageUrl', 'description', 'titre', 'textButton'])
const props = defineProps({
  imageUrl: {
    type: String,
    default: '@/assets/images/BOX.png'
  },
  description: {
    type: String,
    default: "ceci est une description d'une carte"
  },
  titre: {
    type: String,
    default: 'Tailwind card'
  },
  textButton: {
    type: String,
    default: 'En savoir plus ...'
  }
})
</script>
