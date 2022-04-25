<template>
    <div id="app">
        <div>
            <label class="label">Recreative</label>
            <label class="label">'Рекламна мережа'</label>
        </div>
        
            <img :src="img" alt="">
        
        
        <div>
            <h2>{{name}}</h2>
        </div>
    </div>
</template>

<script>
    export default {
        name:'Banner',
        props: {
    img: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
    }
</script>

<style lang="css" scoped>
img{
    margin: 10px;
    height: 180px;
    width: 180px;
}
.label{
   color: red;
   margin-right:  50px; ;
   border: 2px solid black;
   
}
div{
 margin: 10px;
    border: 2px solid black;
    width: 320px;
}
#app{

}
</style>