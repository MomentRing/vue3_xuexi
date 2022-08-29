<template>
    <MyCeshi :car="'奔驰'" @myClick="fn"></MyCeshi>
    <Mycom></Mycom>
</template>

<script setup>
import MyCeshi from './components/MyCeshi.vue'
import Mycom from './components/Mycom.vue'
function fn(val) {
    console.log('从子组件传过来的值是' + val);
}
</script>

<style scoped>
</style>
