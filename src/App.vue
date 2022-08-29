<template>
    <p>{{ format(money, '元') }}</p>
</template>

<script setup>
import { ref } from 'vue'
const money = ref(12000)
function format(money, params) {
    return money + params
}
</script>

<style scoped>
</style>
