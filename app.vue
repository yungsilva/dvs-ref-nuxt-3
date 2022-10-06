<template>
  <div class="page">
    <pre></pre>
    <pre></pre>
    <pre></pre>
  </div>
</template>

<script setup lang="ts">
import { onMounted, createApp } from 'vue'
import Counter from './components/Counter.vue'

onMounted(() => {
  document.querySelectorAll('pre').forEach((preElement) => {
    const wrapper = document.createElement('div')

    const componentApp = createApp(Counter)

    componentApp.mount(wrapper)

    preElement.append(wrapper)
  })
})
</script>
