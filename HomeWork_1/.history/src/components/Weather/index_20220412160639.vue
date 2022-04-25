<template>
    <div>
        <label>
          Назва товару
          <!-- <input type="text" v-model="searchProductTitle" /> -->
          <select v-model="searchCityTitle">
            <option
              v-for="product in wetherData"
              :key="product.id"
              :value="product.title"
            >
              {{ product.title }}
            </option>
          </select>
        </label>
      </div>
    
</template>

<script>
    import Weather from '@/components/Weather';
    
    export default {
        components: {
            Weather
        },
    };
    props:{
        wetherData:{
            type:Array,
            default:()=>[],
        },
    },
    data(){
        return{
          searchCityTitle: null  
        }
    },
    methods:{
        
    }

    }
</script>

<style lang="scss" scoped>

</style>