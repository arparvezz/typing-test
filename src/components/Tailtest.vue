<script setup>
import { ref } from 'vue';
let changeBgColor = ref(false)
let showImage = ref(true)
let showDesc = true;
let darkModeEnable = ref(false)
let n = 1;
</script>
<template>
    <div :class="darkModeEnable?'dark':''" class="bg-gray-100 dark:bg-gray-600 h-screen flex items-center">
        <div class="bg-white dark:bg-slate-600 dark:text-white max-w-sm md:max-w-md mx-auto md:my-auto p-4 md:p-0 rounded text-black text-center space-y-4 md:space-x-4 shadow md:flex overflow-hidden">
            <img v-show="showImage" class="w-50 sm:ring ring-green-400 md:w-1/2 md:h-full cursor-pointer transform duration-300 hover:scale-150" src="https://images.unsplash.com/photo-1491485326079-8713ae1e00a9?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="">
            <div v-if="showDesc" class="space-y-2 md:p-4">
                <div class="space-y-1">
                    <h2 class="text-xl md:text-sm
                     font-bold text-gray-600">Learn Tailwind ✨</h2>
                    <p class="text-sm md:text-xs">Magical CSS framework.</p>
                    <p>{{ Math.floor(Math.random() * 10) }}</p>
                </div>
                <div class="space-x-1">

                <button @click="changeBgColor=!changeBgColor;" class="px-5 py-2 md:text-sm md:px-3 md:py-1 border border-green-400 rounded-full">Change Bg!</button>
                
                <button @click="showImage=!showImage;" class="px-5 py-2 md:text-sm md:px-3 md:py-1  rounded-full transform duration-300 hover:text-purple-600 hover:bg-purple-200 focus:ring-2 focus:ring-purple-700 focus:ring-offset-4">Toggle Image!</button>
            </div>

            </div>
            <button @click="darkModeEnable=!darkModeEnable" class="bg-slate-400 px-3 py-1 rounded">Dark Mode</button>
            
        </div>
    </div>
</template>
<style></style>
