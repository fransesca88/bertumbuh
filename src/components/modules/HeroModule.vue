<template>
  <motion.section
    id="hero"
    class="bg-bertumbuh-light-green relative xl:h-[666px]"
    :initial="{ opacity: 0, y: '50%' }"
    :animate="{
      opacity: 100,
      y: '0%',
      transition: { duration: 0.75, y: { type: 'spring', visualDuration: 0.75, bounce: 0.4 } },
    }"
  >
    <div class="content px-5 xl:px-12 pt-12 xl:max-w-[1000px] flex flex-col gap-12">
      <h1 class="text-bertumbuh-black font-medium">
        <span>Bersama Lindungi Bumi Kita</span>
        <span class="hidden xl:block">untuk Masa Depan</span>
      </h1>
      <p class="text-bertumbuh-black max-w-[500px]">
        Kami bermimpi untuk menanam lebih dari 10 juta pohon dan menciptakan dunia yang lebih indah
        dan asri untuk kita, dia, dan semua.
      </p>
      <div class="ctas flex flex-col md:flex-row gap-6">
        <ButtonComponent type="button" variant="primary" :has-icon="false"
          >Eksplorasi Bertumbuh</ButtonComponent
        >
        <ButtonComponent type="button" variant="secondary" :has-icon="true" icon="play"
          >Lihat Video</ButtonComponent
        >
      </div>
    </div>
    <img src="/images/tree.png" loading="lazy" class="xl:absolute bottom-0 right-0" />
    <div class="sponsor bg-white xl:absolute bottom-0 py-7 xl:pr-20">
      <ul class="uppercase grid grid-cols-2 xl:grid-cols-4 gap-4 xl:gap-10 text-bertumbuh-black/50 font-medium text-2xl xl:text-[28px] text-center xl:text-left">
        <li>Ditlance</li>
        <li>Owthest</li>
        <li>Neovasi</li>
        <li>Onago</li>
      </ul>
    </div>
  </motion.section>
</template>

<script setup lang="ts">
import { motion } from 'motion-v'
import ButtonComponent from '../globals/ButtonComponent.vue'
</script>

<style scoped>
@media screen and (min-width: 1280px){
  .sponsor {
    clip-path: polygon(0 0, calc(100% - 80px) 0, 100% 100px, 100% 100%, 0% 100%);
  }
}
</style>
