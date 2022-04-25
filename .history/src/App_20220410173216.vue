<template>
  <div>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- 3. Використовуємо -->
    <products-list :product-list-data="listData" />
    <weather 
     v-for="weather in weatherData"
      :key="weather.id"
      :city="weather.nameCity"
      
    >
    <hr>
  </div>
</template>

<script>
//1.Імпортуємо компонент
import ProductsList from './components/ProductsList'
// import Weather from './components/Weather'
export default {
  name: 'App',
  components: {
    //2.Реєструємо
    ProductsList,
    // Weather,
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
          productName: 'Олія',
          price:200,
         
        },
      ],
      weatherData:[
        {
          id:12,
          nameCity:'Uzgorod'

        }
      ]
      ,
    }
  },
}
</script>

<style>
#app {
  
  text-align: center;
  
  margin-top: 20px;
}
</style>
