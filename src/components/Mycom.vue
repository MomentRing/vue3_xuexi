<template>
    <button @click="fn1">123</button>
</template>

<script setup>
import mitt from '../mitt'
function fn1() {
    mitt.emit('my-event', 666)
}
</script>

<style scoped>
</style>
