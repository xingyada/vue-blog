<template>
    <div class="swiperDiv">
        <swiper :options="swiperOption" v-if="showSwiper">
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    export default {
        name: 'HomeSwiper',
        props:{
            list:Array
        },
        data: function () {
            return {
                swiperOption: {
                    pagination: '.swiper-pagination',
                    loop: true
                }
            }
        },
        computed:{
            showSwiper(){
                return  this.list.length
            }
        }
    }
</script>

<style lang="stylus" scoped>
.swiperDiv >>> .swiper-pagination-bullet-active
    background:white !important
.swiperDiv 
    height:0
    width:100%
    padding-bottom:40%
    overflow:hidden
    .swiper-img 
        width:100%
</style>