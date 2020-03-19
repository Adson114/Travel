<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题</div>
    <router-link to="/city">
    <div class="header-right">
      {{this.city}}</div>
    </router-link>
    <span class="iconfont arrow-icon" >&#xe64a;</span>
  </div>
</template>

<script>

export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
.header
  display flex
  line-height :$headerHeight
  background : $bgc
  color:#fff
  .header-left
    width :.64rem
    float :left
      .back-icon
        text-align :center
        font-size :.4rem
  .header-input
    flex :1
    line-height .64rem
    margin-top .12rem
    height:.64rem
    margin-left: 2em
    padding-left :.2rem
    background: #fff
    border-radius :0.1rem
    color :#ccc
  .header-right
    width :1.24rem
    float: right
    color :#fff
    text-align :center
      .arrow-icon
        font-size :.24rem
        margin-right :.24rem
</style>
