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
          img: 'https://content2.rozetka.com.ua/goods/images/big_tile/185608067.jpg',
          title: 'Хлібопічка 1',
          price: 1000,
        },
        {
          id: 2,
          img: 'https://content.rozetka.com.ua/goods/images/big_tile/185622291.jpg',
          title: 'Хлібопічка 2',
          price: 2000,
        },
        {
          id: 3,
          img: 'https://content2.rozetka.com.ua/goods/images/big_tile/12600231.jpg',
          title: 'Хлібопічка 3',
          price: 6000,
        },
        {
          id: 5,
          img: 'https://content1.rozetka.com.ua/goods/images/big_tile/63982322.jpg',
          title: 'Хлібопічка 4',
          price: 3000,
        },
        {
          id: 6,
          img: 'https://content2.rozetka.com.ua/goods/images/big_tile/21296941.jpg',
          title: 'Хлібопічка 5',
          price: 67000,
        },
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
