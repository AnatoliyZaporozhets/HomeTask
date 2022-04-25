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
    <div v-for="wether in filteredWetherListData " :key='wether.nameCity'>
            <label>{{weather.day}}</label>
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
           return  console.log(this.wetherData.filter((wether) =>
          wether.nameCity.includes(this.searchCityTitle)
        ));
    //       if (this.searchCityTitle) {
        
    //    
    //   }
    //   return this.wetherData; 
    //     }
    // }

    }}}
</script>

<style lang="scss" scoped>

</style>