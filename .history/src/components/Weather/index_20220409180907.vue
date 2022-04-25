<template>
    <div>
        <label ><input type="text" v-model="cityNam"></label>
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
            city: null,
            day:null
        }
    },
    methods:{
        cityNam(){
            for (const el of this.wetherData) {
                this.city = el.nameCity
            }
        }
    }

    }
</script>

<style lang="scss" scoped>

</style>