<template>
  <HeaderComponent />
  <main class="container mx-auto pt-9 pb-6 px-10 xl:px-0 xl:pt-14 xl:pb-14">
    <slot />
  </main>
  <FooterComponent />
</template>

<script setup lang="ts">
import HeaderComponent from '../globals/HeaderComponent.vue'
import FooterComponent from '../globals/FooterComponent.vue'
</script>

<style scoped></style>
