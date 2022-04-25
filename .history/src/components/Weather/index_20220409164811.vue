<template>
    <div>
        <label >{{nameCity}}</label>
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

    data(){
        return{
            nameCity: null,
            day:null
        }
    },}
</script>

<style lang="scss" scoped>

</style>