<template>
    <div>
        <label>
          Назва міста :
          <select v-model="searchCityTitle" placeholder="Вибеіть місто">
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
      <div v-if="searchCityTitle">
   <div v-for="weather in filteredWetherListData" :key="weather.id">
     <div>День : {{weather.day}}</div>
     <div> Температура : {{weather.temperature}} С</div>
     <div class="weather">
        <h2>Погодні умови : </h2>
           <ul style="list-style-type:none;">
           <li>Вологість:{{weather.humidity}}%</li>
           <li>Тиск:{{weather.atmosphericPressure}}.атм</li>
           <li>Швидкість вітру{{weather.windSpeed}} м/с</li>
         </ul>
      </div>
   </div>
   </div>
   <div v-else>Виберіть місто</div>
</template>

<script>
    export default {
  name: 'Weather',

  props: {
    wetherData: {
      type: Array,
      default: () => [], 
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

<style lang="css" scoped>
.weather{
  border: 2px solid black;
}
</style>