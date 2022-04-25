<template>
    <div>
        <label>
            Post:
            <input type="text"  v-model="post" />
            <button @click='go' :disabled='!post'>Create</button>
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
      },
     methods:{
      go(){
        this.$emit('pushPost',this.post)
        this.post=''
      }
    }  
    }
</script>

<style lang="css" scoped>

</style>