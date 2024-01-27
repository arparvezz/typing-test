<script setup>
import { ref } from 'vue';
let activeIndex = ref(0)
</script>

<template>
    <div class="container mx-auto bg-slate-800 p-4 rounded text-left">
        <div class="item mb-4">
            <h2 @click="activeIndex=0" class="text-xl bg-blue-600 px-4 py-3 rounded cursor-pointer" :class="activeIndex == 0 ? 'bg-green-500': ''">Why Vue JS?</h2>
            <p v-show="activeIndex==0">Truly reactive, compiler-optimized rendering system that rarely requires manual optimization.</p>
        </div>
        <div class="item mb-4">
            <h2 @click="activeIndex=1" class="text-xl bg-blue-600 px-4 py-3 rounded cursor-pointer" :class="activeIndex == 1 ? 'bg-green-500': ''">Why Geo Politics ?</h2>
            <p v-show="activeIndex==1">For predecting our future, we should've proper knowledge about history, geo-politics. You can also use this trics in real life.</p>
        </div>
        <div class="item mb-4">
            <h2 @click="activeIndex=2" class="text-xl bg-blue-600 px-4 py-3 rounded cursor-pointer" :class="activeIndex == 2 ? 'bg-green-500': ''">Why religion ?</h2>
            <p v-show="activeIndex==2">Relion is the complete manual of our life. As a human being everyone should follow a religion.</p>
        </div>
    </div>
</template>

<style scoped>

</style>
