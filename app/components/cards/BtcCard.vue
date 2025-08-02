<template>
  <div
    class="w-40 p-4 rounded-xl bg-gradient-to-br from-black/60 to-zinc-800/60 text-white shadow-xl backdrop-blur-md"
  >
    <div class="flex items-center gap-2 mb-2">
      <img :src="icon" alt="icon" class="w-6 h-6" >
      <div>
        <p class="text-sm font-medium">{{ name }}</p>
        <p class="text-xs text-gray-400">{{ code }}</p>
      </div>
    </div>

    <p class="text-lg font-bold">{{ price }}</p>
    <p class="text-sm text-green-500 font-semibold">{{ change }}</p>

    <div class="mt-2">
      <svg xmlns="http://www.w3.org/2000/svg" width="109" height="51" viewBox="0 0 109 51" fill="none">
        <path d="M1 49.5L8.5 26.5L17 37L22 19.5L31 37L44.5 3L57.5 26.5L72 19.5L83.5 31L93.5 6.5L101 19.5H108" stroke="#1ECB4F" stroke-width="2" stroke-linecap="round"/>
      </svg>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  code: String,
  price: String,
  change: String,
  icon: String,
})
</script>
