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
     {{weather.nameCity}}
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
          searchCityTitle: {
          id:12,
          nameCity:'Ужгород',
          day:12,
          temperature:12,
          humidity:82,
          atmosphericPressure:742,
          windSpeed:2

        }
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