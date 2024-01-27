<script setup>
import { ref,reactive } from 'vue';
let previousText = ref('I had no idea what I wanted to do with my life and no idea how college was going to help me figure it out. And here I was spending all of the money my parents had saved their entire life. So I decided to drop out and trust that it would all work out OK. It was pretty scary at the time, but looking back it was one of the best decisions I ever made. The minute I dropped out I could stop taking the required classes that didn’t interest me, and begin dropping in on the ones that looked interesting.')
let previousTextLength = previousText.value.length;
let correctWord = ref(0)
let wrongWord = ref(0)
let userInput = reactive([])

function checkTypingWord(){
    correctWord.value = 0;
    wrongWord.value = 0;
    for(let i = 0 ; i < userInput.length; i++){
        if(userInput[i] === previousText.value.split('')[i]){
            correctWord.value++;
        }else{
            wrongWord.value++;
        }
    }
}

let showAlert = ref(false)
let time = ref(0)
function startTimer(){
    setInterval(function(){
    if(time.value >= 60) {
        showAlert.value = true;
        return;
    }else{
        time.value +=1;
    }
},1000)
}


function reset(){
    location.reload()
}

</script>
<template>
    <div class="container mx-auto p-4" v-if="showAlert == false">
        <h2 class="text-3xl">Minimal typing game!</h2>
        <h3>Time : {{ time }}</h3>
        <p>Correct word: <span class="text-green-400">{{ correctWord }}</span>, wrong word: <span class="text-red-500">{{ wrongWord }}</span></p>
        <div class="text-slate-500 p-3 ">
           {{ previousText }}
        </div>
        <textarea v-model="userInput" @focus="startTimer()" @input="checkTypingWord();" name="" id="" cols="30" rows="12" class="my-2 w-full p-2 focus:outline-none ring-1 ring-slate-700 bg-transparent " :maxlength="previousTextLength"></textarea>


        
    </div>
    <div v-if="showAlert" class="w-full h-[100vh] bg-green-800 opacity-80 p-10 flex flex-col justify-center items-center">
        <p class="text-xl">You correctly typed <span class="text-2xl text-green-300" v-text="correctWord"></span> letter/minute, But you also mistyped <span v-text="wrongWord" class="text-2xl text-red-300" ></span> letter.</p><br>
        <button class="px-4 py-2 bg-red-700 rounded hover:bg-red-800" @click="reset()">Reset X</button>
    </div>
</template>
<style>
</style>