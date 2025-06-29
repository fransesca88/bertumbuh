<template>
  <div class="bg-[#F6F8FD] flex flex-row items-center px-5 py-2.5">
    <input
      type="text"
      name="search"
      id="search"
      :placeholder="props.textPlaceholder"
      v-bind="$attrs"
    />
    <button type="submit">
      <Search class="text-bertumbuh-black" />
    </button>
  </div>
</template>

<script setup lang="ts">
import { Search } from 'lucide-vue-next'

const props = defineProps({
  textPlaceholder: {
    type: String,
    default: '',
  },
})
</script>

<style scoped></style>
