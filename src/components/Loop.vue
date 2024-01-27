<script setup>
import { ref } from 'vue';

let countries = ref([
    {id:1,name:'Bangladesh',capital:'Dhaka'},
    {id:2,name:'India',capital:'Delhi'},
    {id:3,name:'Pakistan',capital:'Islamabad'},
    {id:4,name:'Nepal',capital:'Kathmundu'},
])

let serverContent = ref([]);
(function getServerContent(){
    fetch('https://jsonplaceholder.typicode.com/users/')
    .then(rawData => rawData.json())
    .then(data => data.forEach(v => serverContent.value.push(v)))
    .catch(err => console.log(err))
})()

let searchText =ref('')

function filteredUser(){ 
    return serverContent
}

function filteringUser(){
    if(searchText != ''){
        filteredUser().value.filter((v)=>{
            if(v.name.includes(searchText)){
                return v
            }
        })
    }else{
        return filteredUser().value;
    }
}

</script>
<template>

    <div class="container mx-auto">
        <input type="text" v-model="searchText" name="search" id="search" class="m-3 border border-slate-400 p-3 rounded" placeholder="search user">
        <p>{{ searchText }}</p>
        <div class="flex justify-between my-1 p-1 rounded bg-green-700" v-for="user in filteredUser().value" :key="user.id">
        <h2>{{ user.name }}</h2>  <h2>{{ user.email }}</h2>
    </div>
    </div>

    

</template>
<style></style>