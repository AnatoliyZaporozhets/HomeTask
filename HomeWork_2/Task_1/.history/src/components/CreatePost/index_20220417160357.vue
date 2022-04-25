<template>
    <div>
        <label>
            Post:
            <input type="text"  v-model="post" />
            <button @push='$emit('pushPost', post )'>Create</button>
        </label>
    </div>
</template>

<script>
    export default {
      name:'CreatePost' ,
      data(){
          return{
              post:''
          }
      } 
    }
</script>

<style lang="css" scoped>

</style>