<template>
    <div>
        <input type="text" name="" id="">
        <button @click="onChange(1)">+</button>
        <button @click="onChange(-1)">-</button>
        <span>{{likes}}</span>
    </div>
</template>

<script>
    export default {
        name:'PostList',

        props: {
            postListArray: {
                type: Array,
                default: ()=>[]
            }
        },
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