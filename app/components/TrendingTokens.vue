<template>
  <section class="bg-[#0F1114]">
    <div
      class="xl:w-[1300px] w-full mx-auto px-4 xl:px-0 py-8 lg:pt-[60px] lg:pb-32"
    >
      <!-- Header -->
      <div
        class="flex flex-col lg:flex-row lg:justify-between lg:items-end mb-[60px]"
      >
        <div>
          <h2
            class="font-bold text-3xl lg:text-4xl text-bcoin-primary leading-11 tracking-[0%] mb-5"
          >
            Most Trending Tokens
          </h2>
          <p
            class="text-base lg:text-lg leading-[30px] text-white mb-4 lg:mb-0"
          >
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. <br />
            Lorem Ipsum has been the industry's standard
          </p>
        </div>
        <button
          class="w-fit flex items-center py-2 lg:py-[13px] px-5 lg:px-9 gap-2.5 border border-[#B4B4B4] rounded-xl"
        >
          <p
            class="font-semibold text-sm lg:text-base text-[#B4B4B4] leading-6 tracking-[0%]"
          >
            Market Overview
          </p>
          <img
            src="/images/trending-token-img/right-arrow-svg.svg"
            alt="right arrow"
          />
        </button>
      </div>

      <div class="">
        <!-- Content -->
        <div class="grid grid-cols-1 lg:grid-cols-3 lg:gap-x-6 gap-y-6">
          <!-- Left panel: Tabs & Table -->
          <div class="col-span-2 bg-[#1E2329] rounded-lg p-5">
            <!-- Tabs -->
            <div class="flex items-center space-x-8 mb-4">
              <button
                class="font-medium text-lg text-light-gray hover:text-ivory-white leading-[30px] border-b hover:border-bcoin-primary hover:cursor-pointer pb-2"
              >
                Hot Derivatives
              </button>
              <button
                class="font-medium text-lg text-light-gray hover:text-ivory-white leading-[30px] border-b hover:border-bcoin-primary hover:cursor-pointer pb-2"
              >
                Hot Coins
              </button>
            </div>

            <!-- Table -->
            <div class="overflow-x-auto">
              <table class="w-full">
                <thead>
                  <tr class="text-xs text-light-gray tracking-[0%] text-center">
                    <th class="text-left pl-3 py-[9px]">Trading Pairs</th>
                    <th class="py-[9px]">Last Traded Price</th>
                    <th class="py-[9px]">24H Change</th>
                    <th class="py-[9px]">Charts</th>
                    <th class="pr-3 py-[9px]">Trade</th>
                  </tr>
                </thead>
                <tbody class="text-ivory-white">
                  <tr
                    v-for="(item, index) in trades"
                    :key="index"
                    class="group text-center"
                  >
                    <td
                      class="pl-3 py-[18px] flex items-center group-hover:bg-[#CDE8FE40]/20 gap-2 group-hover:rounded-l-[5px] group-hover:cursor-pointer"
                    >
                      <img :src="item.icon" class="w-5 h-5" alt="" />
                      {{ item.pair }}
                    </td>
                    <td
                      class="py-[18px] group-hover:bg-[#CDE8FE40]/20 group-hover:cursor-pointer"
                    >
                      {{ item.price }}
                    </td>
                    <td
                      class="py-[18px] group-hover:bg-[#CDE8FE40]/20 group-hover:cursor-pointer"
                      :class="
                        item.change > 0 ? 'text-green-400' : 'text-red-400'
                      "
                    >
                      {{ item.change > 0 ? "+" : "" }}{{ item.change }}%
                    </td>
                    <td
                      class="xl:pl-20 md:pl-8 py-[18px] group-hover:bg-[#CDE8FE40]/20 group-hover:cursor-pointer"
                    >
                      <img
                        :src="
                          item.change > 0
                            ? '/images/trending-token-img/emerald-green-small-graph-svg.svg'
                            : '/images/trending-token-img/crimson-red-small-graph-svg.svg'
                        "
                        class="w-[47px] h-5"
                        alt="chart"
                      />
                    </td>
                    <td
                      class="pr-3 py-[18px] group-hover:bg-[#CDE8FE40]/20 group-hover:rounded-r-[5px] group-hover:cursor-pointer"
                    >
                      <button
                        class="font-medium group-hover:text-charcoal-black text-bcoin-primary text-sm leading-5 tracking-[0%] px-[10px] py-[1px] border-[0.5px] group-hover:border-none border-bcoin-primary bg-[#F7A6001A] group-hover:bg-bcoin-primary group-hover:cursor-pointer rounded-md"
                      >
                        Trade
                      </button>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <!-- Right Panel -->
          <div class="bg-[#1E2329] rounded-lg p-5">
            <!-- Top Gainers -->
            <div class="mb-[25px]">
              <p
                class="font-medium text-lg text-ivory-white leading-[30px] tracking-[0%]"
              >
                Top Gainers
              </p>
              <div
                v-for="(g, i) in gainers"
                :key="i"
                class="flex justify-between items-center font-medium text-sm text-ivory-white leading-5 tracking-[0%] py-[14px]"
              >
                <div class="flex items-center gap-2">
                  <img :src="g.icon" class="w-5 h-5" alt="" />
                  {{ g.name }}
                </div>
                <p>{{ g.price }}</p>
                <p :class="g.change > 0 ? 'text-green-400' : 'text-red-400'">
                  {{ g.change > 0 ? "+" : "" }}{{ g.change }}%
                </p>
                <img
                  :src="
                    g.change > 0
                      ? '/images/trending-token-img/emerald-green-small-graph-svg.svg'
                      : '/images/trending-token-img/crimson-red-small-graph-svg.svg'
                  "
                  class="w-10 h-3"
                  alt="chart"
                />
              </div>
            </div>

            <!-- New Listings -->
            <div>
              <p
                class="font-medium text-lg text-ivory-white leading-[30px] tracking-[0%]"
              >
                New Listings
              </p>
              <div
                v-for="(l, i) in listings"
                :key="i"
                class="flex justify-between items-center font-medium text-sm text-ivory-white leading-5 tracking-[0%] py-[14px]"
              >
                <div class="flex items-center gap-2">
                  <img :src="l.icon" class="w-5 h-5" alt="" />
                  {{ l.name }}
                </div>
                <p>{{ l.price }}</p>
                <p :class="l.change > 0 ? 'text-green-400' : 'text-red-400'">
                  {{ l.change > 0 ? "+" : "" }}{{ l.change }}%
                </p>
                <img
                  :src="
                    l.change > 0
                      ? '/images/trending-token-img/emerald-green-small-graph-svg.svg'
                      : '/images/trending-token-img/crimson-red-small-graph-svg.svg'
                  "
                  class="w-10 h-3"
                  alt="chart"
                />
              </div>
            </div>
          </div>
        </div>

        <!-- CTA -->
        <div
          class="flex flex-col lg:flex-row lg:justify-between lg:items-center mb-[60px] mt-[120px]"
        >
          <div>
            <h2
              class="font-bold text-3xl lg:text-4xl text-bcoin-primary leading-11 tracking-[0%] mb-5"
            >
              Most Trending Tokens
            </h2>
            <p
              class="text-base lg:text-lg leading-[30px] text-white mb-4 lg:mb-0"
            >
              Unlock new opportunities with Zaptrade. Stay informed, track
              market trends, and make <br />
              your next big trade with confidence and ease.
            </p>
          </div>
          <button
            class="w-fit flex items-center py-2 lg:py-[13px] px-5 lg:px-9 gap-2.5 bg-bcoin-primary rounded-xl"
          >
            <p
              class="font-semibold text-sm lg:text-base text-charcoal-black leading-6 tracking-[0%]"
            >
              Get Started
            </p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="11"
              height="12"
              viewBox="0 0 11 12"
              fill="none"
            >
              <path
                d="M10.8754 0.879548L3.10924 0.879548C2.95606 0.879549 2.80437 0.90972 2.66285 0.968342C2.52132 1.02696 2.39273 1.11289 2.28441 1.22121C2.17609 1.32952 2.09017 1.45812 2.03155 1.59964C1.97293 1.74117 1.94275 1.89285 1.94275 2.04604C1.94275 2.19922 1.97293 2.35091 2.03155 2.49244C2.09017 2.63396 2.17609 2.76255 2.28441 2.87087C2.39273 2.97919 2.52132 3.06511 2.66285 3.12374C2.80437 3.18236 2.95606 3.21253 3.10924 3.21253L6.8925 3.21253L0.63437 9.47066C0.415578 9.68945 0.292661 9.9862 0.292661 10.2956C0.292661 10.605 0.415578 10.9018 0.634371 11.1206C0.853163 11.3394 1.14991 11.4623 1.45933 11.4623C1.76875 11.4623 2.06549 11.3394 2.28429 11.1206L8.54242 4.86245L8.54242 8.6457C8.54198 8.79901 8.57185 8.95089 8.63032 9.09262C8.68878 9.23434 8.77469 9.36311 8.8831 9.47151C8.9915 9.57992 9.12027 9.66583 9.26199 9.72429C9.40371 9.78276 9.5556 9.81263 9.70891 9.81219C10.0183 9.81215 10.3149 9.68923 10.5337 9.47048C10.7524 9.25174 10.8754 8.95506 10.8754 8.6457L10.8754 0.879548Z"
                fill="#1C1C1E"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { trades } from "../../data/data";
import { gainers } from "../../data/data";
import { listings } from "../../data/data";
</script>
