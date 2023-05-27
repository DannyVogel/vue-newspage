<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>

    <div class="w-full h-16 bg-blue-300 flex justify-between items-center px-4">
      <h1>W.</h1>

      <nav class="w-48 flex justify-around bg-blue-900">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/pinia">Pinia</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
