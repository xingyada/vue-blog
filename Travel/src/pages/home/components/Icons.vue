<template>
    <div class="icons">
        <swiper :options="swiperOption" v-if="showPages">
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item in page" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl" alt="">
                    </div>
                    <p class="icon-desc">{{ item.desc }}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
    export default {
        name: 'HomeIcons',
        props:{
            list: Array
        },
        data() {
            return {
                swiperOption: {
                    pagination: '.swiper-pagination',
                    //loop: true
                }
            }
        },
        computed: {
            pages () {
                const pages = []
                this.list.forEach((item, index) => {
                    const page = Math.floor(index / 8)
                    if (!pages[page]) {
                        pages[page] = []
                    }
                    pages[page].push(item)
                })
                return pages
            },
            showPages(){
                return this.list.length
            }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
    width:100%
    height:0
    padding-bottom:50%

.icons
    overflow:hidden
    width:100%
    height:0
    padding-bottom:50%
    .icon 
        position:relative
        overflow:hidden
        float:left
        width:25%
        height:0
        padding-bottom:25%
        .icon-img
            position:absolute
            top:0
            left:0
            right:0
            bottom:0.44rem
            box-sizing:border-box
            padding: .1rem
            .icon-img-content
                height:100%
                display:block
                margin:0 auto
        .icon-desc
            position:absolute
            left:0
            right:0
            bottom:0
            height:.44rem
            text-align:center
            ellipsis()
</style>