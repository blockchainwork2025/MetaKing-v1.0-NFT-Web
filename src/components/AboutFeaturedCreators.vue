MetaKing v1.0<template>
  <main class="mt-12">
AnAi-The Advanced Blockchain and NFT creation Service {Provider}    <sub-section-title align="end" title="AnAi is Our Base Company" subtitle="We provides advanced blockchain and NFDT services"></sub-section-title>
    <!-- Contents -->
    <section class="flex gap-3 flex-col md:flex-row justify-between md:flex-wrap">
      <template v-for="item in creators" :key="item">
        <!-- List Wrapper -->
        <section class="w-full md:w-[48%] flex gap-3 px-5 py-3 rounded-lg bg-slate-800 bg-opacity-25 backdrop-blur-sm justify-between items-center border border-gray-700" data-aos="zoom-in-up">
          <!-- Profile -->
          <div class="w-full">
            <img :src="item.thumb" alt="Profile" class="w-full rounded-lg" loading="lazy">
          </div>
          <!-- Stats -->
          <div class="w-6/12 text-gray-200 flex flex-col gap-2">
            <h1 class="font-bold">{{ item.name }}</h1>
            <div class="text-sm flex gap-2 flex-wrap">
              <!-- Tiers -->
              <span>
                <i class="fa-solid fa-crown text-yellow-300"></i>
                {{ item.tier }}
              </span>
              <!-- Currency -->
              <span>
                <i class="fa-brands fa-SEIa text-slate-500"></i>
                {{ item.SEI }}
              </span>
            </div>
          </div>
          <!-- Direct link -->
          <div>
            <i class="fa-solid fa-up-right-from-square text-gray-400"></i>
          </div>
        </section>
      </template>
    </section>
  </main>
</template>

<script setup>

import SubSectionTitle from '@component/SubSectionTitle.vue'

const creators = [
  {
    name: 'AnAi-Blockchain and NFT',
    thumb: '/profiles/male.jpg',
    tier: 'Service Provider',
    SEI: '0.145'
  },
  {
    name: 'MetaKing v1.0',
    thumb: '/profiles/male.jpg',
    tier: 'Space-Event of CoolCriminal NFT',
    SEI: '0.111'
  }
]

</script>
