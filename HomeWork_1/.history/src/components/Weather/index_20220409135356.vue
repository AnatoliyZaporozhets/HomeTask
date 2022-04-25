<template>
    <div>

    </div>
</template>

<script>
    // import Weather from "./Weather"
    export default {
  name: 'ProductList',

  components: {
    Weather,
  },

  props: {
    productListData: {
      type: Array,
      default: () => [], //Якщо об"єкт - то функція, що повертає значення
    },
  },
}
</script>

<style lang="scss" scoped>

</style>