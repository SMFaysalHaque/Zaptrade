<template>
  <div
    class="group relative bg-[#1E2329] px-[17px] py-5 lg:px-[35px] lg:py-10 border border-white/10 rounded-xl overflow-hidden max-w-[360px] transition-all duration-500 ease-in-out hover:max-w-[500px]"
  >
    <img class="mb-5" :src="icon" :alt="title" />
    <p class="font-semibold text-2xl text-white mb-[67px]">{{ title }}</p>
    <p class="text-xl text-gray-400 mb-[67px]">
      {{ description }}
    </p>
  </div>
</template>

<script setup>
const props = defineProps({
  title: String,
  description: String,
  icon: String
});
</script>
