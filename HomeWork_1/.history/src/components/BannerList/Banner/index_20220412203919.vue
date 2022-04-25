<template>
    <div>
        <div>
            <label >Recreative</label>
            <label >'Рекламна мережа'</label>
        </div>
        <div>
            <img href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSk21azxKyx0qXvegHq3pSXs49D-UCsi5gBQg&usqp=CAU">
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