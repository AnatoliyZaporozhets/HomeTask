<template>
    <div>
        <div>
            <label class="label">Recreative</label>
            <label class="label">'Рекламна мережа'</label>
        </div>
        <div>
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
.label{
   color: red;
   height: 70px;
   border: 2px solid black;
}
div{
 margin-top: 10px;
}
</style>