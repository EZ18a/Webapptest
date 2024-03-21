<script setup>
import {ref} from 'vue'
const title= ref('testタイトル')
let price = ref(9)

function increment(){
price.value+=1
}

function hen(){
title.value='変更したね'
}

function mou(){
title.value=(title.value =='変更したね' ? '変更したの' : '変更してないの')
}
</script>

<template>
<h1>Title : {{title}}</h1>
<h2>Price : {{price -1}}</h2>
<button @click="increment">{{title}}</button>
<button @click='hen'>title変更{{price}}</button>
<button @click='mou'>もう一回変更していいよ。</button>
</template>

<style>
h2{
color : red;
}
</style>
