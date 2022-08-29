<template>
    <button @click="add">{{ count }}</button>
    <p>{{ a }}</p>
    <button @click="add1">age++</button>
    <p>{{ obj.age }}</p>
</template>
    
<script setup>
import { ref } from 'vue'
let count = ref(0)
let a = ref(10)
const obj = ref({
    age: 18
})
function add() {
    count.value++
    console.log(count);
}
function add1() {
    obj.value.age++
}
</script>
    
<style>
</style>