<template>
    <button @click="add">{{ count }}</button>
</template>
    
<script >
export default {
    data() {
        return {
            count: 0
        }
    },
    methods: {
        add() {
            this.count++
        }
    }
}
</script>
    
<style>
</style>