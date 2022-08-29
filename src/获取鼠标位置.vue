<template>
    <p>x坐标为{{ obj.x }},y坐标为{{ obj.y }}</p>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
const obj = ref({
    x: 0,
    y: 0
})
const fn = (e) => {
    obj.value.x = e.pageX
    obj.value.y = e.pageY
}
// 相当于mounted
onMounted(() => {
    document.documentElement.addEventListener('mousemove', fn)
})

// 相当于beforedestroyed
onUnmounted(() => {
    document.documentElement.removeEventListener('mousemove', fn)
})

</script>

<style scoped>
</style>
