<template>
  <RouterLink
    :to="props.link"
    class="text-bertumbuh-black transition-all border-b-2 border-b-bertumbuh-green/0 ease-in-out duration-150 hover:border-b-bertumbuh-green"
    exact-active-class="border-b-2 border-b-bertumbuh-green text-bertumbuh-green"
  >
    <slot>{{ props.label }}</slot>
  </RouterLink>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'

const props = defineProps({
  link: {
    type: String,
    default: '',
  },
  label: {
    type: String,
    default: '',
  },
})
</script>

<style scoped></style>
