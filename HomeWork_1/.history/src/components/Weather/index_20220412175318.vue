<template>
    <div>
        <label>
          Назва міста :
          <!-- <input type="text" v-model="searchProductTitle" /> -->
          <select v-model="searchCityTitle">
            <option
              v-for="wether in wetherData"
              :key="wether.id"
              :value="wether.nameCity"
            >
              {{wether.nameCity}}
            
            </option>
          </select>
        </label>
      </div>
   <div v-for="weather in filteredWetherListData" :key="weather.id">
     <div>День : {{weather.day}}</div>
     <div> Температура : {{weather.temperature}} С</div>
     <div>
        <h2>Погодні умови : </h2>
           <ul style="list-style-type:none;">
           <li>Вологість:{{weather.humidity}}%</li>
           <li>Тиск:{{weather.atmosphericPressure}}.атм</li>
           <li>Швидкість вітру{{weather.windSpeed}} м/с</li>
         </ul>
      </div>
   </div>
</template>

<script>
    export default {
  name: 'Weather',

  props: {
    wetherData: {
      type: Array,
      default: () => [], //Якщо об"єкт - то функція, що повертає значення
    },
  },

    data(){
        return{
          searchCityTitle: null 
        }
    },
    computed:{
        filteredWetherListData(){
           return  this.wetherData.filter((wether) =>
          wether.nameCity.includes(this.searchCityTitle
        ));
    }}}
</script>

<style lang="scss" scoped>

</style>