<template>
    <div id="app">
        <div>
            <label class="label">Recreative</label>
            <label class="label">'Рекламна мережа'</label>
        </div>
        <div class="img-container">
            <img :src="img" alt="">
        </div>
            
        
        
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
#app {
  border: 2px solid red;
  border-radius: 8px;
  padding: 10px;
  width: 230px;
  text-align: center;
}

img {
  width: 215px;
  margin: 10px;
}
label{
      border: 2px solid red;
      margin-right: 14px;

}
</style>