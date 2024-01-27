<script setup>
import { ref } from 'vue';
let mark = ref(0)
let questions = ref([
    {name:'What is JavaScript ?',clues:['Scripting language','Markup Language','Stylesheet Language'], ans:'Scripting language'},
    {name:'What is Vue ?',clues:['JS Library','JS Framework','Typescript lang'], ans:'JS Library'},
    {name:'What is WordPress ?',clues:['CMS','Language','Hardware'], ans:'CMS'}
    ])

    // function checkMark(){
    //     mark.value = 0;
    //     questions.forEach(question => {
    //         if(question.checkedvalue == question.ans){
    //             mark.value += 5;
    //         }
    //     })
    // }
</script>
<template>

    <div class="container mx-auto p-5">
        <h4>Total Mark : {{ mark }}</h4>
        <div class="my-2 p-3 bg-slate-600 rounded" v-for="(question,index) in questions" :key="index">
            <h2>{{ question.name }}</h2>

            <select name="input" id="input" v-model="question.clues">
                <option v-for="(clue,index) in question.clues" :key="index" :value="clue">{{ clue }}</option>
            </select>

            
        </div>
    </div>

</template>
<style></style>