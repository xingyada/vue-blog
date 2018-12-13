<template>
    <div>
        <div class="title">周末游</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src='item.imgUrl' />
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'HomeWeekend',
        data: function () {
            return {
                recommendList: [{
                    id: '0001',
                    imgUrl: 'https://dimg07.c-ctrip.com/images/w30i0o000000enulf6C20.jpg_Z_800_600.jpg',
                    title: '地名1',
                    desc: '地名的一个简单介绍sdkbksksjbksbksdjhskksjbkbvdkbk啊啊啊啊啊啊啊啊'
                }, {
                    id: '0002',
                    imgUrl: 'https://dimg07.c-ctrip.com/images/w30i0o000000enulf6C20.jpg_Z_800_600.jpg',
                    title: '地名2',
                    desc: '地名的一个简单介绍sdkbksksjbksbksdjhskksjbkbvdkbk啊啊啊啊啊啊啊啊'
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
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 60%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>