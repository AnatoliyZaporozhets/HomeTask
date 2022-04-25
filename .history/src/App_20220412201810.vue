<template>
  <div>
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- 3. Використовуємо -->
    <products-list :product-list-data="listData" />
    <hr>
    <weather 
     :wetherData='weatherDataList'
    />
    <hr>
    <banner-list 
    :bannerDataList='bannerDataList'
    />
    
  </div>
</template>

<script>
//1.Імпортуємо компонент
import ProductsList from './components/ProductsList'
import Weather from './components/Weather'
import BannerList from './components/BannerList'
export default {
  name: 'App',
  components: {
    //2.Реєструємо
    ProductsList,
    Weather,
    BannerList
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
      weatherDataList:[
        {
          id:12,
          nameCity:'Ужгород',
          day:12,
          temperature:12,
          humidity:82,
          atmosphericPressure:742,
          windSpeed:2

        },
        {
          id:13,
          nameCity:'Київ',
          day:13,
          temperature:13,
          humidity:83,
          atmosphericPressure:743,
          windSpeed:3

        },
        {
          id:14,
          nameCity:'Харків',
          day:14,
          temperature:14,
          humidity:84,
          atmosphericPressure:744,
          windSpeed:4

        },
      ]
      ,
      bannerDataList:[
        {
          id:1,
          name:'Шипшина',
          img:'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSk21azxKyx0qXvegHq3pSXs49D-UCsi5gBQg&usqp=CAU',
        },
      ]
    }
  },
}
</script>

<style>
#app {
  
  /* text-align: center; */
  
  margin-top: 20px;
}
</style>
