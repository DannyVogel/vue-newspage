<script setup>
import {useCounterStore} from '../stores/counter'
const store = useCounterStore()
</script>

<template>
  <main>
    <h1>Testing Pinia!</h1>
    <p>Count is {{ store.count }}</p>
    <p>Double count is {{ store.doubleCount }}</p>
    <button @click="store.increment">Increment</button>
  </main>
</template>