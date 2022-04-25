<template>
    <div>
        <label ><input type="text">{{city}}</label>
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
        },
    },
    data(){
        return{
            city: null,
            
        }
    },
    methods:{
        cityNam(){
            return this.city
        }
    }

    }
</script>

<style lang="scss" scoped>

</style>