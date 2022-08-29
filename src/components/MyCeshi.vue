<template>
    {{ car }}
    <button @click="$emit('myClick', 100)">100</button>
    <button @click="fn">200 </button>
</template>

<script setup>
import mitt from '../mitt'
mitt.on('my-event', (num) => {
    console.log(num);
})
const props = defineProps({
    car: {
        type: String,
        required: true
    }
})
const emit = defineEmits(['myClick'])
function fn() {
    emit('myClick', 200)
}
</script>

<style scoped>
</style>
