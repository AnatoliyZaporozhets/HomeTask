<template>
  <div>
    <create-post @pushPost='pushArr' />
    <post-list v-for="(post,index) in postListArr" :key="index" :posts='post.post'/>
    
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
        this.postListArr.push({post : inp})
        console.log(this.postListArr);
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
