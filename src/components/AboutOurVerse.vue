<template>
  <main class="mt-12">
    <sub-section-title align="end" title="Hands" subtitle="Welcome to our verse, your new journey start here"></sub-section-title> 
    <!-- Caraousels -->
    <Splide class="mb-6" :options="{ rewind: true, autoplay: true }" aria-label="My Favorite Images" data-aos="zoom-in-up">
      <template v-for="slide in 7" :key="slide">
        <SplideSlide class="w-full">
        <img class="rounded-lg w-full" :src="getImage(slide)" alt="hands">
        </SplideSlide>
      </template>
    </Splide>
    <!-- Content -->
    <section class="flex flex-wrap justify-between gap-5">
      <template v-for="(item, x) in Hands" :key="x">
        <p data-aos="zoom-in-up" v-html="item" class="inline-block md:w-[48%] text-gray-200"></p>
      </template>
    </section>
  </main>
</template>

<script setup>

import { Splide, SplideSlide } from '@splidejs/vue-splide'
import SubSectionTitle from '@component/SubSectionTitle.vue'
import hands from '@content/hands.js'
import '@splidejs/vue-splide/css'

const getImage = num => `/verse/wasaka-town-${num}.png`

</script>
