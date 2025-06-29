<template>
  <button
    :type="type"
    class="py-2 px-5 transition-all shadow-none hover:shadow-lg ease-in-out duration-300 cursor-pointer"
    vbind="$attrs"
    :class="{
      'bg-bertumbuh-green text-white shadow-bertumbuh-green/40': props.variant == 'primary',
    }"
  >
    <slot>{{ props.label }}</slot>
  </button>
</template>

<script setup lang="ts">
type TButton = {
  label?: string
  type: 'button' | 'submit' | 'reset'
  variant: 'primary' | 'normal'
}

const props = defineProps<TButton>()
</script>

<style scoped></style>
