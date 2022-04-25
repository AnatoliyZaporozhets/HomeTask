<template>
    <div>
        <label>{{posts}}</label>
        <button @click="onChange(1)">Like</button>
        <button @click="onChange(-1)">Dislike</button>
        <span>Likes : {{likes}}</span>
    </div>
</template>

<script>
    export default {
        name:'PostList',

        props: {
            posts: {
                type: String,
                default: ''
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