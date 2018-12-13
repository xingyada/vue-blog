<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="list in recommendList" :key = "list.id">
                <img class="item-img" :src="list.imgUrl" />
                <div class="item-info">
                    <p class="item-title">{{list.title}}</p>
                    <p class="item-desc">{{list.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>    
<script>
    export default {
        name : 'HomeRecommend',
        data (){
            return {
                recommendList : [{
                    id: 'recom001',
                    imgUrl: 'http://imgs.qunarzz.com/ftejia/1806/f9/8a23740f5a6f86.jpg',
                    title: '地名',
                    desc: '一个简单的介绍，总部设在驻马店，十一人民九个骗啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊'
                }, {
                    id: 'recom002',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
                    title: '故宫',
                    desc: '一个简单的介绍，总部设在驻马店，十一人民九个骗啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊'
                }, {
                    id: 'recom003',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_250x250_ecfa0df2.jpg',
                    title: '水立方',
                    desc: '一个简单的介绍，总部设在驻马店，十一人民九个骗啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊'
                }]
            }
        }
    }
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'

.title
    margin-top: .2rem
    line-height: .8rem
    background : #eee
    text-indent: .2rem
.item
    overflow:hidden
    display:flex
    height:1.9rem
    .item-img
        width:1.7rem
        height:1.7rem
        padding: .1rem
    .item-info
        flex: 1
        min-width: 0
        padding: .1rem
       .item-title
            line-height: .54rem
            font-size: .32rem
            ellipsis()
      .item-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
      .item-button
            line-height: .44rem
            margin-top: .16rem
            background: #ff9300
            padding: 0 .1rem
            border-radius: .06rem
            color: #fff
</style>