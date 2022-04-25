<template>
    <div>
        <div>
            <label >Recreative</label>
            <label >'Рекламна мережа'</label>
        </div>
        <div>
            <img :src="img">
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
    // title1: {
    //   type: String,
    //   default: 'Recreative', 
    // },
    // title2: {
    //   type: String,
    //   default: 'Рекламна мережа', 
    // },
  },
    }
</script>

<style lang="scss" scoped>

</style>