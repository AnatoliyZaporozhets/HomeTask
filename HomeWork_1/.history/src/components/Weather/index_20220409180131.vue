<template>
    <div>
        <label ><input type="text" v-model="nameCity"></label>
    </div>
    <div>
        
        <weather-indicators>
    </div>
</template>

<script>
    import WeatherIndicators from "./WeatherIndicators"
    export default {
     name: 'Weather',
     components: {
        //2.Реєструємо
     WeatherIndicators,
    },
    props:{
        wetherData:{
            type:Array,
            default:()=>[],
        }
    },
    data(){
        return{
            nameCity: null,
            day:null
        }
    },
    methods:{
        cityNam(){
            return this.nameCity = this.wetherData.nameCity
        }
    }

    }
</script>

<style lang="scss" scoped>

</style>