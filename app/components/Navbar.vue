<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <div class="lg:w-[1440px] w-full flex items-center justify-between ">
            <img class="w-[198px] h-14" src="../assets/logo.png" alt="logo">
            <div class="hidden lg:flex items-center text-ivory-white py-7 gap-10">
                <div>
                    Buy Crypto
                </div>
                <div>
                    Markets
                </div>
                <div class="flex items-center gap-[5px]">
                    <p>
                        Trade
                    </p>
                    <svg xmlns="http://www.w3.org/2000/svg" width="15" height="20" viewBox="0 0 15 20" fill="none">
                        <path d="M2.5 8L7.45 12.95L12.4 8" stroke="#FDFDFD" stroke-width="1.65" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </div>
                <div>
                    Futures
                </div>
                <div class="flex items-center gap-[5px]">
                    <p>
                        Earn
                    </p>
                    <svg xmlns="http://www.w3.org/2000/svg" width="15" height="20" viewBox="0 0 15 20" fill="none">
                        <path d="M2.5 8L7.45 12.95L12.4 8" stroke="#FDFDFD" stroke-width="1.65" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </div>
            </div>
            <div class="hidden lg:flex items-center gap-5">
                <svg class="w-[74px] h-[50px] py-[14px] px-[26px]" xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 26 26" fill="none">
                    <path d="M11.625 21.25C16.9408 21.25 21.25 16.9408 21.25 11.625C21.25 6.30927 16.9408 2 11.625 2C6.30927 2 2 6.30927 2 11.625C2 16.9408 6.30927 21.25 11.625 21.25Z" stroke="#FDFDFD" stroke-width="3.41657"/>
                    <path d="M24 24L19.875 19.875" stroke="#FDFDFD" stroke-width="3.41657" stroke-linecap="round"/>
                </svg>
                <button class="font-semibold text-charcoal-black py-2 px-9 bg-bcoin-primary rounded-xl">
                    Sign Up
                </button>
                <button class="font-semibold text-charcoal-black py-2 px-9 bg-ivory-white rounded-xl">
                    Sign In
                </button>
            </div>
            <!-- Hamburger Button (Mobile) -->
            <button class="lg:hidden" @click="toggleMenu">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" fill="none" viewBox="0 0 24 24">
                <path stroke="#fff" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
            </button>
        </div>
        <!-- Mobile Sidebar Menu -->
        <transition name="slide">
            <div
                v-if="isMenuOpen"
                class="fixed inset-0 z-50 bg-black bg-opacity-95 p-6 flex flex-col gap-6 text-white"
            >
                <div class="flex justify-between items-center mb-6">
                <img class="w-[150px]" src="../assets/logo.png" alt="logo" >
                <button @click="toggleMenu">
                    <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" fill="none" viewBox="0 0 24 24">
                    <path stroke="#fff" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
                </div>
                <div>Buy Crypto</div>
                <div>Markets</div>
                <div class="flex items-center gap-1">
                <p>Trade</p>
                <svg xmlns="http://www.w3.org/2000/svg" width="15" height="20" viewBox="0 0 15 20" fill="none">
                    <path d="M2.5 8L7.45 12.95L12.4 8" stroke="#FDFDFD" stroke-width="1.65" stroke-linecap="round" stroke-linejoin="round" />
                </svg>                                    
                </div>
                <div>Futures</div>
                <div class="flex items-center gap-1">
                <p>Earn</p>
                <svg xmlns="http://www.w3.org/2000/svg" width="15" height="20" viewBox="0 0 15 20" fill="none">
                    <path d="M2.5 8L7.45 12.95L12.4 8" stroke="#FDFDFD" stroke-width="1.65" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
                </div>
                <div class="flex flex-col gap-4 mt-6">
                <button class="py-2 px-4 bg-bcoin-primary rounded-xl text-black font-semibold">
                    Sign Up
                </button>
                <button class="py-2 px-4 bg-white rounded-xl text-black font-semibold">
                    Sign In
                </button>
                </div>
            </div>
        </transition>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.3s ease;
}
.slide-enter-from,
.slide-leave-to {
  transform: translateX(100%);
}

</style>