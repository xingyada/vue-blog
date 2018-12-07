<template>
    <div class="header">
        <div class="header-left">
            <div class="icon iconfont icon-fanhui"></div>
        </div>
        <div class="header-input">
            <span class="icon iconfont icon-sousuo"></span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="icon iconfont icon-xiangxia"> </span>
        </div>
    </div>
</template>

<script>    
export default {
    name : 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/variables.styl'
    .header
      display:flex
      line-height: 0.86rem
      background: $bgColor
      color:#fff
      .header-left
        width: .64rem
        float: left
        .icon
            text-align:center
            font-size: .4rem
      .header-input
        flex:1
        background:#fff
        border-radius: .1rem
        line-height: .64rem
        height: .64rem
        margin-top: .12rem
        margin-left:.2rem
        color:#ccc
      .header-right
        width:1.24rem
        float:right
        text-align:center
        .icon
            margin-left: -.04rem
            font-size: .24rem
</style>