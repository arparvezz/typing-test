<script setup>
import { ref,reactive } from 'vue';
let questions = reactive([
    {title:'Is you alive',ans:true},
    {title:'Are you adult',ans:true},
    {title:'Are you coding?',ans:false}
])
let mark = ref([])

function checkMark(){
    // mark = 0;
    questions.forEach(q => {
        if(q.ans == String(q.input)){
            mark.push(1)
        }
    })

}

</script>
<template>
    <div class="container mx-auto p-5">
        <div class="p-4 border border-slate-500" v-for="(question,index) in questions" :key="question">
        <h2>{{ question.title }}</h2>
        <input type="radio" :name="index" id="true" value="true" v-model="question.input">true
        <input type="radio" :name="index" :id="index" value="false" v-model="question.input">false
        </div>
        <button @click="checkMark()" class="my-4 px-4 py-2 bg-green-700 rounded hover:bg-green-900">check mark</button>
        <p>Total Mark : {{ mark }}</p>
    </div>
</template>
<style>
</style>