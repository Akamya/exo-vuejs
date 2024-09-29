<script setup>
import { defineProps } from "vue";
const props = defineProps({
  size: {
    type: String,
    default: () => "medium",
  },
});
</script>

<template>
  <p
    class="font-serif"
    :class="{
      'text-red-500 text-2xl': props.size === 'small',
      'text-gray-500 text-3xl': props.size === 'medium',
      'text-blue-500 text-4xl': props.size === 'big',
    }"
  >
    <slot></slot>
  </p>
</template>
