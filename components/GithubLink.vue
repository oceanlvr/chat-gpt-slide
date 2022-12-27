<script setup lang="ts">
// import { useFetch } from '@vueuse/core'

const props = defineProps({
  title: {
    default: 'null'
  },
  url: { default: '' },
})
// const repo = props.url.replace('https://github.com/', 'https://api.github.com/repos/')

// const { isFetching, error, data } = useFetch(repo)
// const { stargazers_count = 0 } = data as any

</script>

<template>
  <a :href="url">
    {{ title }}<carbon:logo-github />
  </a>
</template>
