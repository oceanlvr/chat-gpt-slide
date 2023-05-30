<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  title: {
    default: null
  },
  img: { default: '', },
  url: { default: '' }
})

const title = ref(props.title)
const jump = (url) => window.open(url)
</script>

<template>
  <div @click="jump(url)" cursor="pointer" overflow-auto border="~ gray-400 opacity-50 rounded-md">
    <div>
      <img :src="img" w="~" h="100%"/>
    </div>
    <div v-if="title" text-center>
      {{ title }}
    </div>
  </div>
</template>
