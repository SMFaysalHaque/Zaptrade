<template>
  <div class="bg-black/60 backdrop-blur-lg p-4 rounded-xl shadow-lg w-56 text-white">
    <div class="flex items-center justify-between">
      <span class="font-semibold">{{ name }}</span>
      <svg class="w-5 h-5 text-yellow-500" fill="currentColor" viewBox="0 0 20 20">
        <path d="M10 2L4 10h4v6l6-8h-4z" />
      </svg>
    </div>
    <div class="mt-2 text-lg font-bold">{{ price }}</div>
    <div :class="{'text-green-400': isPositive, 'text-red-400': !isPositive}">
      {{ change }}
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  name: String,
  price: String,
  change: String
})

const isPositive = computed(() => props.change.startsWith('+'))
</script>
