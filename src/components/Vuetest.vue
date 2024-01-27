<script setup>
import { ref } from 'vue';
let showContent = ref(false);
let minimize = ref(false)
let dropdown = ref(false)
let score = ref(0)
let adjective = ref('Awesome')

let randomArr = [ 
    'Awesome',
    'superb',
    'amazing',
    'cool'
]



</script>
<template>
    <div class="container mx-auto">
        <p class="bg-blue-500 hover:bg-blue-700 inline-block px-3 rounded-full ">I'm {{ adjective }}</p>
        <button class="my-4 block bg-green-500 px-3 py-1 rounded">Set random 💞</button>
    </div>


    <!-- <div class="container mx-auto relative">
        <button @click="showContent=!showContent;minimize=true" class="mt-2 bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded">⏹</button>
        <nav v-if="showContent" class="max-w-[200px] h-screen bg-slate-300 text-black flex flex-col space-y-4 my-3 p-4 absolute top-0 right-0" :class="minimize ? 'bg-green-200' : ''">
            <button @click="minimize=!minimize" class="text-right">-</button>
            <button @click="showContent=false" class="text-right">x</button>
            <a v-show="minimize" class="hover:bg-slate-400 px-4 py-2 rounded" href="#">Joke</a>
            <a v-show="minimize" class="hover:bg-slate-400 px-4 py-2 rounded" href="#">Film</a>
            <a v-show="minimize" class="hover:bg-slate-400 px-4 py-2 rounded" href="#">Drama</a>
        </nav>
        <p>Get up man</p>
    </div> -->
    <!-- <div class="container mx-auto">
        <nav class="py-3 px-3 space-x-4">
            <a href="#">Home</a>
            <a @click="dropdown=!dropdown" href="#" class="relative">Services <span v-show="dropdown==false">🔽</span></a>
            <div v-show="dropdown" class="dropdown absolute top-10 left-14 flex flex-col bg-slate-500 p-3 rounded" >
                <a href="#">Web design</a>
                <a href="#">Graphic design</a>
            </div>
            <a href="#">Contact</a>
        </nav>
        <p>Your score is: <span>{{ score }}</span></p>
        <button @click="score++" class="bg-blue-500 p-2 rounded mt-3 ring ring-red-400 hover:ring-red-800">Increase - {{ score }}</button>
    </div> -->

    <!-- <div class="h-screen flex justify-center items-center">
        <div class="max-w-sm bg-white text-black p-4 rounded">
            <h2 v-if="showContent" class="text-2xl">Vue JS.</h2>
            <p v-else class="text-red-600">Content Hidden</p>
            <p v-show="showContent" >Don't call me</p>
            <button @click="showContent=!showContent" class="mt-2 bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded">Where content matter!</button>
    </div>
    </div>-->

   
</template>
<style></style>