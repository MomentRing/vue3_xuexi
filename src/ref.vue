<template>
    <MyCeshi :car="'奔驰'" @myClick="fn"></MyCeshi>
    <Mycom></Mycom>
    <p ref="Myref">168</p>
</template>

<script setup>
import MyCeshi from './components/MyCeshi.vue'
import Mycom from './components/Mycom.vue'
import { onMounted, ref } from 'vue'
function fn(val) {
    console.log('从子组件传过来的值是' + val);
}


const Myref = ref(null)
onMounted(() => {
    console.log(Myref.value.innerHTML);
})
</script>

<style scoped>
</style>
