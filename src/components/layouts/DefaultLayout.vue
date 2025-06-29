<template>
  <HeaderComponent />
  <main>
    <slot />
  </main>
  <FooterComponent />
</template>

<script setup lang="ts">
import HeaderComponent from '../globals/HeaderComponent.vue'
import FooterComponent from '../globals/FooterComponent.vue'
</script>

<style scoped></style>
