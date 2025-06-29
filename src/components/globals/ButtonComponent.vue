<template>
  <button
    :type="type"
    class="group py-2 px-5 transition-all shadow-none hover:shadow-lg ease-in-out duration-300 cursor-pointer border-2 border-bertumbuh-green flex flex-row items-center justify-center"
    vbind="$attrs"
    :class="{
      'bg-bertumbuh-green text-white shadow-bertumbuh-green/40': props.variant == 'primary',
      'bg-bertumbuh-green/0 text-bertumbuh-black hover:bg-bertumbuh-green hover:text-white border-2 shadow-bertumbuh-green/40':
        props.variant == 'secondary',
      'gap-2': props.hasIcon,
    }"
  >
    <span v-if="props.hasIcon">
      <span v-if="slots.icon">
        <slot name="icon" />
      </span>

      <Play
        class="text-bertumbuh-green group-hover:text-white group-hover:fill-white"
        v-else-if="props.icon === 'play'"
      />
      <ArrowRight class="text-bertumbuh-green" v-else-if="props.icon === 'arrow'" />
    </span>

    <slot>{{ props.label }}</slot>
  </button>
</template>

<script setup lang="ts">
import { useSlots, type Component } from 'vue'
import { Play, ArrowRight } from 'lucide-vue-next'

type TButton =
  | {
      label?: string
      type: 'button' | 'submit' | 'reset'
      variant: 'primary' | 'secondary'
      hasIcon: false
    }
  | {
      label?: string
      type: 'button' | 'submit' | 'reset'
      variant: 'primary' | 'secondary'
      hasIcon: true
      icon?: 'play' | 'arrow'
      customIcon?: never
    }
  | {
      label?: string
      type: 'button' | 'submit' | 'reset'
      variant: 'primary' | 'secondary'
      hasIcon?: true
      icon?: never
      customIcon: Component
    }

const props = defineProps<TButton>()
const slots = useSlots()
</script>

<style scoped></style>
