<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import Accordion from './components/Accordion.vue';
import Condition from './components/Condition.vue';
import Tailtest from './components/Tailtest.vue';
import Vuetest from './components/Vuetest.vue';
// import Loop from './components/Loop.vue';
// import Quiz from './components/Quiz.vue';
import NewQuiz from './components/NewQuiz.vue';
import Typinggame from './components/Typinggame.vue';
</script>

<template>
  <!-- <div class="container mx-auto">
    <button @click="con = !con" class="bg-blue-600 px-4 py-2 rounded mb-4 hover:bg-blue-700 transition duration-300">Toggle Element</button>
    <h3 v-if="con" :class="con ? 'bg-green-600': '' ">Heading: Hello Vue</h3>
    <p v-else="con" :class="!con ? 'bg-red-600': '' ">Paragraph: Lorem ipsum dolor sit amet.</p>

    
  </div> -->
  <!-- <Accordion/> -->
  <!-- <HelloWorld msg="Vite + Vue" /> -->
  <!-- <Condition/> -->
  <!-- <Tailtest/> -->
  <!-- <Vuetest/> -->
  <!-- <Loop/> -->
  <!-- <Quiz/> -->
  <!-- <NewQuiz/> -->
  <Typinggame/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
