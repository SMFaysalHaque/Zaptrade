<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="relative w-full min-h-screen overflow-hidden">
    <!-- Background videos -->
    <video
      autoplay
      loop
      muted
      playsinline
      class="absolute top-0 left-0 w-full h-full object-cover hidden xl:block z-0"
    >
      <source src="/images/b-herosections v1.mp4" type="video/mp4" />
    </video>
    <video
      autoplay
      loop
      muted
      playsinline
      class="absolute top-0 left-0 w-full h-full object-cover xl:hidden z-0"
    >
      <source src="/images/b-herosections v2.mp4" type="video/mp4" />
    </video>

    <!-- Content grid -->
    <div
      class="relative z-10 w-full min-h-screen grid grid-cols-1 xl:grid-cols-2 items-center px-4 sm:px-8 md:px-12 xl:px-20 py-10"
    >
      <!-- Left content -->
      <div class="text-white space-y-6 text-center xl:text-left">
        <p
          class="font-semibold text-3xl sm:text-4xl md:text-5xl xl:text-[65px] leading-tight"
        >
          Build Wealth with <br />
          Crypto
        </p>

        <p class="text-gray-300 max-w-md mx-auto xl:mx-0 text-sm sm:text-base">
          Join the growing community on Zaptrade — the trusted destination for
          effortless crypto investing and trading.
        </p>

        <div
          class="flex flex-col sm:flex-row sm:items-center gap-4 justify-center xl:justify-start"
        >
          <!-- Signup input -->
          <div
            class="flex border border-bcoin-primary rounded-lg overflow-hidden w-full sm:w-auto"
          >
            <input
              type="text"
              placeholder="Email/Phone number"
              class="flex-grow px-4 py-2 bg-transparent text-white outline-none"
            />
            <button class="bg-bcoin-primary text-black font-semibold px-4">
              Sign Up
            </button>
          </div>

          <p>or</p>

          <!-- Social buttons -->
          <div
            class="flex items-center justify-center gap-[15px] p-[15px] bg-[#1E2329] border border-[#4A4A4A] rounded-lg"
          >
            <button
              class="bg-white rounded-full w-9 h-9 flex items-center justify-center"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="34"
                height="34"
                viewBox="0 0 34 34"
                fill="none"
              >
                <g clip-path="url(#clip0_1_338)">
                  <path
                    d="M33.3422 13.7359H31.9997V13.6667H16.9997V20.3334H26.4188C25.0447 24.2142 21.3522 27 16.9997 27C11.4772 27 6.99967 22.5225 6.99967 17C6.99967 11.4775 11.4772 7.00004 16.9997 7.00004C19.5488 7.00004 21.868 7.96171 23.6338 9.53254L28.348 4.81837C25.3713 2.04421 21.3897 0.333374 16.9997 0.333374C7.79551 0.333374 0.333008 7.79587 0.333008 17C0.333008 26.2042 7.79551 33.6667 16.9997 33.6667C26.2038 33.6667 33.6663 26.2042 33.6663 17C33.6663 15.8825 33.5513 14.7917 33.3422 13.7359Z"
                    fill="#FFC107"
                  />
                  <path
                    d="M2.255 9.24251L7.73084 13.2583C9.2125 9.59001 12.8008 7.00001 17 7.00001C19.5492 7.00001 21.8683 7.96168 23.6342 9.53251L28.3483 4.81834C25.3717 2.04418 21.39 0.333344 17 0.333344C10.5983 0.333344 5.04667 3.94751 2.255 9.24251Z"
                    fill="#FF3D00"
                  />
                  <path
                    d="M16.9996 33.6666C21.3046 33.6666 25.2163 32.0191 28.1738 29.34L23.0154 24.975C21.2862 26.2908 19.1726 27.0023 16.9996 27C12.6646 27 8.98378 24.2358 7.59711 20.3783L2.16211 24.5658C4.92044 29.9633 10.5221 33.6666 16.9996 33.6666Z"
                    fill="#4CAF50"
                  />
                  <path
                    d="M33.3425 13.7359H32V13.6667H17V20.3334H26.4192C25.7618 22.1804 24.5778 23.7943 23.0133 24.9759L23.0158 24.9742L28.1742 29.3392C27.8092 29.6709 33.6667 25.3334 33.6667 17C33.6667 15.8825 33.5517 14.7917 33.3425 13.7359Z"
                    fill="#1976D2"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_1_338">
                    <rect width="34" height="34" fill="white" />
                  </clipPath>
                </defs>
              </svg>
            </button>
            <button class="">
              <!-- Apple icon -->
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="28"
                height="34"
                viewBox="0 0 28 34"
                fill="none"
              >
                <path
                  d="M23.3294 32.6359C21.5202 34.4301 19.5448 34.1468 17.6434 33.2969C15.6311 32.4281 13.785 32.3904 11.662 33.2969C9.00359 34.4679 7.60055 34.1279 6.0129 32.6359C-2.99608 23.136 -1.66689 8.66891 8.56053 8.14008C11.0528 8.27229 12.7881 9.53768 14.2465 9.651C16.4249 9.19773 18.511 7.89456 20.8371 8.06454C23.6247 8.29118 25.7293 9.42437 27.1139 11.4641C21.354 14.9959 22.7201 22.7582 28 24.9302C26.9477 27.7632 25.5816 30.5773 23.3109 32.6548L23.3294 32.6359ZM14.0619 8.02676C13.785 3.81507 17.1264 0.339957 20.9663 0C21.5017 4.87272 16.6465 8.49893 14.0619 8.02676Z"
                  fill="#FDFDFD"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Right floating cards -->
      <div
        class="relative w-full h-[400px] sm:h-[500px] xl:h-full mt-10 xl:mt-0"
      >
        <div class="absolute top-[245px] left-[31px] hidden sm:block">
          <CryptoCard
            name="Litecoin"
            code="LTC"
            price="$8,291"
            change="+0.25%"
            icon="/litecoin.svg"
          />
        </div>

        <div class="absolute top-[145px] right-[153px]">
          <CryptoCard
            name="Bitcoin"
            code="BTC"
            price="$52,291"
            change="+0.25%"
            icon="/bitcoin.svg"
          />
        </div>

        <div class="absolute bottom-[116px] left-[160px] hidden sm:block">
          <CryptoCard
            name="Ethereum"
            code="ETH"
            price="$28,291"
            change="+0.25%"
            icon="/ethereum.svg"
          />
        </div>

        <div class="absolute bottom-[439px] right-[41px]">
          <CryptoCard
            name="Ripple"
            code="XRP"
            price="$9,291"
            change="+0.25%"
            icon="/ripple.svg"
          />
        </div>

        <div class="absolute bottom-[240px] right-[86px]">
          <CryptoCard
            name="Ripple"
            code="XRP"
            price="$9,291"
            change="+0.25%"
            icon="/ripple.svg"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import CryptoCard from "./cards/CryptoCard.vue";
</script>
