<template>
    <div>
        <input type="text" name="" id="">
        <button @click="onChange(1)">+</button>
        <button @click="onChange(-1)">-</button>
        <input type="number">
    </div>
</template>

<script>
    export default {
        name:'PostList',
    data(){
        return{
            likes:0
        }
    },
    methods: {
    onChange(increment) {
      this.likes+=increment
    },

    }}
    
</script>

<style lang="scss" scoped>

</style>