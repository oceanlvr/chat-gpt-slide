<script setup lang="ts">

const props = defineProps({
  title: {
    default: 'null'
  },
  url: { default: '' },
})

</script>

<template>
  <a :href="url">
    {{ title }}<carbon:book />
  </a>
</template>
