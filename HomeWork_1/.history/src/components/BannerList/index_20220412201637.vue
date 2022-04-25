<template>
    <div>
        <banner v-for="banner in bannerListData" :key="banner.id"
        :img='banner.imf'
        :name='banner.name'
        :title1='banner.title1'
        :title2='banner.title2'
        />
    </div>
</template>

<script>
import Banner from '@/components/Banner.vue'
 export default {
        name: 'BannerList',
        
        components:{
            Banner,
        },
    props:{
        bannerListData:{
            type: Array,
            default:()=>[]
        },
        },
    }
    
</script>

<style lang="css" scoped>

</style>