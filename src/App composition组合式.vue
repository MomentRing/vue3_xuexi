<template>
    <button @click="add">{{ count }}</button>
</template>
    
<script >
export default {
    setup() {
        let count = 0
        function add() {
            count++
            console.log(count);
        }
        return {
            count,
            add
        }
    }

}
</script>
    
<style>
</style>