<template>
  <div class="counter">
    <p>counter: {{ count }}</p>
    <button @click="count++">increment</button>
  </div>
</template>

<script setup lang="ts">
const count = useState('count', () => 0)

// works fine 👇
// const count = ref(0)
</script>

<style scoped>
.counter {
  border: 1px solid #ccc;
  width: max-content;
  padding: 1rem;
}
</style>
