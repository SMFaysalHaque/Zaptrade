<template>
  <div
    class="bg-[#1E1E1E]"
    :style="`background-image: url(${bgImage}); background-repeat: no-repeat; background-size: cover;`"
  >
    <div
      class="xl:w-[1300px] w-full mx-auto px-4 xl:px-0 py-8 lg:pt-[60px] lg:pb-32"
    >
      <p
        class="font-bold lg:text-4xl text-2xl text-ivory-white text-center leading-11 tracking-[0%] lg:mb-[60px] mb-8"
      >
        Why Zaptrade?
      </p>

      <div
        v-for="card in cards"
        :key="card.id"
        class="flex flex-wrap lg:flex-nowrap justify-center md:justify-start xl:justify-center gap-4"
      >
        <WhyCard
          :title="card.title"
          :description="card.description"
          :icon="card.icon"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import bgImage from "../assets/zaptrade-img/bg-image.png";
import { cards } from "../data/data";
import WhyCard from "./cards/WhyCard.vue";
</script>
