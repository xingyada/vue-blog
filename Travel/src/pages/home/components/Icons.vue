<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide>
                <div class="icon" v-for="item in iconList" :key="item.id">
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
        data() {
            return {
                iconList: [{
                    id: '0001',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    desc: '红门'
                }, {
                    id: '0002',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                    desc: '红门2'
                }, {
                    id: '0003',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                    desc: '红门2'
                }, {
                    id: '0004',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/5e/c640ec3b7d7ae802.png',
                    desc: '红门2'
                }, {
                    id: '0005',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/f6/e54fad3ea337b02.gif',
                    desc: '红门2'
                }, {
                    id: '0006',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
                    desc: '红门2'
                }, {
                    id: '0007',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
                    desc: '红门红门红门红门'
                }, {
                    id: '0008',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
                    desc: '红门8'
                }, {
                    id: '0009',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc: '红门2'
                    }],
                swiperOption: {
                    pagination: '.swiper-pagination',
                    //loop: true
                }
            }
        },

        computed: {
            pages () {
                const pages = []
                this.iconList.forEach((item, index) => {
                    const page = Math.floor(index / 8)
                    if (!pages[page]) {
                        pages[page] = []
                    }
                    pages[page].push(item)
                })
                return pages
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