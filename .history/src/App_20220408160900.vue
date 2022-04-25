<template>
  <div>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- 3. Використовуємо -->
    <products-list :product-list-data="listData" />
  </div>
</template>

<script>
//1.Імпортуємо компонент
import ProductsList from './components/ProductsList'
export default {
  name: 'App',
  components: {
    //2.Реєструємо
    ProductsList,
  },

  data() {
    return {
      listData: [
        {
          id: 1,
          productName: 'Сир',
          price: 100,
         
        },
        {
          id: 2,
          productName: 'Сщр',
          price:200,
         
        },
      ],
    }
  },
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
