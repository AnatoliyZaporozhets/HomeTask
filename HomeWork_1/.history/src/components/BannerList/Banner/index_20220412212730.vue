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
  margin: 10px;
  padding: 10px;
}
.img-container {
  height: 120px;
}
img {
  width: 250px;
}
</style>