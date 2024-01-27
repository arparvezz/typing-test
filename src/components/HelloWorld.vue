<script setup>
import { ref } from 'vue';

let showHeading = ref(true);
let showDesc = ref(true)
</script>

<template>
  <div class="container my-3 bg-slate-700 p-4 font-mono rounded text-left">
    <h2 v-show="showHeading" class="text-2xl">Vue is awesome!</h2>
    <p v-show="showDesc" >An approachable, performant and versatile framework for building web user interfaces.</p>
  </div>
  <button v-on:click="showHeading=false" class="bg-blue-600 hover:bg-blue-700 mr-2">hide heading</button>
  <button @click="showDesc=!showDesc">Toggle Desc</button>
  <button @click="showDesc=true;showHeading=true" class="bg-green-500 ml-2">Reset</button>
</template>

<style scoped>

</style>
