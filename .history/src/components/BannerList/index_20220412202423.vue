<template>
    <div>
        <banner v-for="banner in bannerListData" :key="banner.id"
        :img='banner.imf'
        :name='banner.name'
        
        />
    </div>
</template>

<script>
import Banner from '@/components/Banner'
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