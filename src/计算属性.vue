<template>
    <input v-model.number="a">
    <input v-model.number="b">
    <p>{{ c }}</p>
    <input v-model.number="num">
    <input v-model.number="num1">
</template>

<script setup>
import { ref, computed } from 'vue'
let a = ref('')
let b = ref('')
let c = computed(() => {
    return a.value + b.value
})
let num = ref('')
let num1 = computed({
    get() {
        return Math.pow(num.value, 2)
    },
    set(newVal) {
        num.value = Math.sqrt(newVal, 2)
    }
})
</script>

<style scoped>
</style>
