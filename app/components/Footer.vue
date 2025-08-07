<template>
  <div class="bg-[#1E1E1E] relative overflow-hidden">
    <!-- Background Images -->
    <div class="absolute inset-0 z-0">
      <!-- Background Image 1 - Top left area -->
      <div class="absolute top-[239px] left-0 w-1/2 h-1/2">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="906"
          height="311"
          viewBox="0 0 906 311"
          fill="none"
        >
          <g opacity="0.5" clip-path="url(#clip0_1_150)">
            <g style="mix-blend-mode: overlay">
              <path
                d="M-49.7609 311.004L-51 310.001L-12.4356 262.308L13.314 301.737L54.166 238.786L100.43 185.813L130.511 234.35L164.334 205.281L209.536 277.845L233.393 233.408L285.736 174.712L316.594 118.631L334.354 157.344L385.13 99.7663L424.785 32.2309L443.541 62.14L476.246 0L494.147 27.993L513.207 0.98803L570.729 163.124L625.988 58.4561L651.48 101.047L674.081 88.2734L674.494 88.8733L738.109 181.296L782.035 135.709L808.558 162.898L873.903 69.6314L906 118.133L904.676 119.012L873.868 72.4579L808.759 165.386L782.042 137.996L737.904 183.805L737.35 183.001L673.597 90.3765L650.911 103.196L626.073 61.6989L570.443 167.076L512.738 4.4179L494.08 30.8442L476.376 3.16522L443.661 65.3264L424.831 35.2974L386.411 100.698L333.927 160.23L316.463 122.166L287.028 175.622L234.689 234.311L209.638 281.02L163.964 207.698L130.137 236.771L100.211 188.481L55.4333 239.742L13.3175 304.655L-12.5733 265.007L-49.7609 311.004Z"
                fill="#6b7280"
              />
            </g>
          </g>
          <defs>
            <clipPath id="clip0_1_150">
              <rect
                width="957"
                height="311"
                fill="white"
                transform="translate(-51)"
              />
            </clipPath>
          </defs>
        </svg>
      </div>

      <!-- Background Image 2 - Center right area -->
      <div class="absolute top-0 right-0">
        <img src="/images/footer-img/Solana_Camera6.png" />
      </div>

      <!-- Background Image 3 - Bottom area -->
      <div class="absolute bottom-0 left-0">
        <img src="/images/footer-img/Dai_Camera2.png" />
      </div>
    </div>

    <div
      class="relative z-10 xl:w-[1300px] w-full mx-auto px-4 xl:px-0 py-8 lg:py-[69px]"
    >
      <div>
        <h2
          class="text-3xl md:text-4xl text-ivory-white font-bold leading-11 tracking-[0%] mb-[59px]"
        >
          Stay connected. Trade wherever <br class="md:block hidden" />
          you are.
        </h2>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-2">
        <div class="space-y-8 lg:space-y-12 order-2 lg:order-1">
          <div class="space-y-6">
            <div
              class="flex flex-col md:flex-row lg:flex-col items-start md:items-center lg:items-start xl:gap-0 gap-[60px] xl:pt-0 pt-10"
            >
              <div
                class="flex items-center gap-7 xl:mb-[60px] lg:pl-[50px] xl:pl-[81px] bg-transparent"
              >
                <img
                  class="xl:w-[209px] w-[150px]"
                  src="/images/footer-img/qr-code.png"
                  alt="qr code"
                />

                <div>
                  <p
                    class="xl:text-lg text-md text-[#E0E0E0CC] leading-6 tracking-[0%] mb-5"
                  >
                    Scan to Download App
                  </p>
                  <h3
                    class="font-semibold xl:text-2xl text-xl text-light-gray leading-8 tracking-[0%]"
                  >
                    <span class="underline">iOS</span> &
                    <span class="underline">Android</span>
                  </h3>
                </div>
              </div>

              <div class="flex gap-[50px] lg:pl-[50px] xl:pl-[81px]">
                <img
                  class="xl:w-full w-[60px]"
                  src="/images/footer-img/apple-icon.png"
                  alt="apple logo"
                />

                <img
                  class="xl:w-full w-[80px]"
                  src="/images/footer-img/windows-icon.png"
                  alt="windows logo"
                />
              </div>
            </div>
          </div>
        </div>

        <!-- Right Content Section - Trading Interface - Order 1 on mobile/tablet, 2 on desktop -->
        <div class="relative order-1 xl:order-2">
          <img
            class="w-full"
            src="/images/footer-img/video-img.png"
            alt="video image"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Add any component logic here if needed
</script>

<style scoped>
/* Additional custom styles if needed */
</style>
