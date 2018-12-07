<template>
    <div class="swiperDiv">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide>
                <img class="swiper-img" src="https://img.nike.com.hk/resources/template/heroProductRotatingModule/20181204180953.jpg"
                    alt="">
            </swiper-slide>
            <swiper-slide>
                <img class="swiper-img" src="https://img.nike.com.hk/resources/template/heroProductRotatingModule/20181129102030.jpg"
                    alt="">
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    export default {
        name: 'HomeSwiper',
        data: function () {
            return {
                swiperOption: {
                    pagination: 'swiper-paginatin',
                    loop: true
                }
            }
        },
    }
</script>

<style lang="stylus" scoped>
.swiperDiv 
    height:0
    width:100%
    padding-bottom:40%
    overflow:hidden
    .swiper-img 
        width:100%
</style>