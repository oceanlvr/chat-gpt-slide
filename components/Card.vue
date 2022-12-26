<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  title: {
    default: 'null'
  },
  img: { default: '', },
  url: { default: '' },
  desc: { default: '' },
})

const title = ref(props.title)
const jump = (url) => window.open(url)
</script>

<template>
  <div h="15vh" @click="jump(url)" flex flex-row gap-0 cursor="pointer" border="~ gray-400 opacity-50 rounded-md">
    <div text-left flex-1 p-4>
      <div>
        {{ title }}
      </div>
      <div text-gray leading-4 text-ellipsis indent-4 text-10px font-400>
        {{ desc }}
      </div>
    </div>
    <div>
      <img :src="img" w="~" h="100%" />
    </div>
  </div>
</template>
