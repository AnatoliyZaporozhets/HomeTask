<template>
  <div class="list-container">
    <product-card
      v-for="product in productListData"
      :key="product.id"
      :imageSource="product.img"
      :title="product.title"
      :price="product.price"
    />
  </div>
</template>

<script>
import ProductCard from './ProductCard'
export default {
  name: 'ProductList',

  components: {
    ProductCard,
  },

  props: {
    productListData: {
      type: Array,
      default: () => [], //Якщо об"єкт - то функція, що повертає значення
    },
  },
}
</script>

<style lang="css" scoped>
.list-container {
  display: flex;
}
</style>
