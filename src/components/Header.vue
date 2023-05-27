<script setup>
import { RouterLink } from 'vue-router'
import { ref, computed } from 'vue'

const menuOpen = ref(false)

const toggleMenu = () => {
    menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
    menuOpen.value = false
}

const slideOutMenuClass = computed(() => {
    return menuOpen.value ? 'translate-x-0' : 'translate-x-full'
})

const grayOutBgClass = computed(() => {
    return menuOpen.value ? 'translate-x-0' : 'translate-x-full'
})
</script>

<template>
    <header class="font-sans text-2xl">
        <div class="w-full h-16 flex justify-between items-center px-4">
            <img src="../assets/logo.svg" alt="W. logo">
            <img src="../assets/icon-menu.svg" alt="menu icon" @click="toggleMenu">
            <div id="slide-out-menu" :class="slideOutMenuClass" class="fixed top-0 right-0 h-full w-64 bg-white px-6 transform transition-transform duration-300 ease-in-out overflow-y-auto flex flex-col justify-start">
                <div class="h-16 flex justify-end items-center">
                    <img src="../assets/icon-menu-close.svg" alt="close icon" @click="closeMenu">
                </div>
                <nav class="flex flex-col justify-around gap-y-6 mt-16">
                    <RouterLink to="/">Home</RouterLink>
                    <RouterLink to="/about">About</RouterLink>
                    <RouterLink to="/pinia">Pinia</RouterLink>
                </nav>
            </div>
        </div>
    </header>
</template>

