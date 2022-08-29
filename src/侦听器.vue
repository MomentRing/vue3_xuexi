<template>
    <input v-model="username">
    <p :style="{ color: isValid ? 'green' : 'red' }">{{ isValid ? '合法' : '非法' }}</p>
</template>

<script setup>
import { ref, watch, watchEffect } from 'vue'
let username = ref('')
let isValid = ref(true)
watch(username, (newVal) => {
    if (newVal.length > 8 || newVal.length < 3) {
        isValid.value = false
    } else {
        isValid.value = true
    }
})
watchEffect(() => {
    console.log(username);
})
</script>

<style scoped>
</style>
