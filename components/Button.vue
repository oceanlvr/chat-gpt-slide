<script setup lang="ts">

const props = defineProps({
  title: {
    default: 'null'
  },
  url: { default: '' },
})
const jump = (url) => window.open(url)

</script>

<template>
  <button @click="jump(url)" cursor="pointer" text-xs text-left bg-black hover:bg-slate-800 text-white font-light py-2
    px-4 rounded font-mono>
    <slot></slot>
    {{ title }}
  </button>
</template>
