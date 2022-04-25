<template>
    <div>
        <div>
            <label >Recreative</label>
            <label >'Рекламна мережа'</label>
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
label{
    background-color: red
    ;
    display: flex;
    height: 70px;
    width: 30px;
}
</style>