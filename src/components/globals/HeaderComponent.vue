<template>
  <header id="header" class="pt-9 pb-6 shadow-lg">
    <div class="above pb-0 xl:px-14 xl:pb-9">
      <div class="container mx-auto">
        <div
          class="wrapper flex flex-row justify-center xl:justify-between items-center gap-12 xl:gap-0"
        >
          <div class="mobile-nav flex items-center xl:hidden">
            <button type="button" @click="toggleMobileNav" class="cursor-pointer">
              <Menu v-if="!mobileNavExpanded" />
              <X v-else />
            </button>
          </div>
          <a class="logo flex flex-row-reverse xl:flex-row gap-12 xl:gap-3 items-center" href="/">
            <LogoColored />
            <span class="text-2xl font-semibold">BERTUMBUH</span>
          </a>
          <div class="search-cta hidden xl:flex xl:flex-row xl:gap-5 xl:items-center">
            <div class="search">
              <SearchboxComponent text-placeholder="Cari blog dan artikel disini ..." />
            </div>
            <div class="cta">
              <ButtonComponent type="button" variant="primary">Bergabung</ButtonComponent>
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr class="hidden xl:block border-1 text-bertumbuh-black/40" />
    <div class="below px-14 pt-4 hidden xl:block">
      <div class="container mx-auto">
        <nav id="header-main-navigation">
          <ul class="flex flex-row gap-10">
            <li v-for="menuItem in mainNavigations" :key="menuItem.label.toLowerCase()">
              <NavMenuItemComponent :link="menuItem.link">{{
                menuItem.label
              }}</NavMenuItemComponent>
            </li>
          </ul>
        </nav>
      </div>
    </div>
    <div
      id="mobile-navigation"
      class="px-14 mt-0 h-0 relative overflow-hidden transition-all duration-105"
      :class="{ 'mt-6 h-fit': mobileNavExpanded }"
    >
      <nav id="header-main-navigation">
        <ul class="flex flex-col gap-5">
          <li v-for="menuItem in mainNavigations" :key="menuItem.label.toLowerCase()">
            <NavMenuItemComponent :link="menuItem.link">{{ menuItem.label }}</NavMenuItemComponent>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { Menu, X } from 'lucide-vue-next'
import LogoColored from '../logos/LogoColored.vue'
import ButtonComponent from './ButtonComponent.vue'
import NavMenuItemComponent from './NavMenuItemComponent.vue'
import SearchboxComponent from './SearchboxComponent.vue'

const mainNavigations = [
  {
    label: 'Home',
    link: '/',
  },
  {
    label: 'Kemitraan',
    link: '/kemitraan',
  },
  {
    label: 'Tentang',
    link: '/tentang',
  },
  {
    label: 'Kami Butuh Kamu',
    link: '/kami-butuh-kamu',
  },
  {
    label: 'Post',
    link: '/posts',
  },
  {
    label: 'Newsletter',
    link: '/newsletter',
  },
] as const

const mobileNavExpanded = ref(false)

function toggleMobileNav() {
  mobileNavExpanded.value = !mobileNavExpanded.value
}
</script>

<style scoped></style>
