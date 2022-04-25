<template>
  <div>
    <create-post @pushPost='pushArr' />
    <post-list/>
    <post-list/>
  </div>
</template>

<script>
import CreatePost from './components/CreatePost'
import PostList from './components/PostList'
export default {
  name: 'App',
  components: {
   CreatePost,
   PostList
  },
  data(){
    return{
      postListArr:[],
    }
    
  },
  methods:{
      pushArr(inp){
        this.postListArr.push(inp)
      }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
