<template>
    <div>
        <label >{{nameCity}}</label>
    </div>
    <div>
        
        <weather-indicators>
    </div>
</template>

<script>
    import WeatherIndicators from "./components./WeatherIndicators"
    export default {
     name: 'App',
     components: {
        //2.Реєструємо
     WeatherIndicators,
    },

    data(){
        return{
            nameCity: null,
        }
    },
</script>

<style lang="scss" scoped>

</style>