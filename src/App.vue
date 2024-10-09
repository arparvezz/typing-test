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
