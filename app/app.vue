<template>
  <div>
    <Navbar class="fixed top-0 z-50 bg-navbar-bg opacity-100 w-full inline-flex justify-center pr-4 py-4 xl:pr-0 xl:py-0" />
    <NuxtPage />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue"
import Footer from "./components/Footer.vue";

</script>

<style scoped>

</style>

