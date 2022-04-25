<template>
    <div>
        <input type="text" name="" id="">
        <button @click="onChange(1)">+</button>
        <button @click="onChange(-1)">-</button>
        <!-- <input type="number" v-model="likes"> -->
        <span >{{likes}}</span>
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