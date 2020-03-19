<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">
            {{item.title}}
          </p>
          <p class="item-desc">{{item.desc}}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/bb4e26c0-2d6b-43f4-a525-2b1e14875ae4.jpg_r_480x320x90_bbfe8901.jpg',
        title: '上海-名古屋 5天自由行',
        desc: '赠一晚酒店💕上海🛫名古屋5-7日自由行🎁代办签证代办签证代办签证代办签证代办签证代办签证'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/bb4e26c0-2d6b-43f4-a525-2b1e14875ae4.jpg_r_480x320x90_bbfe8901.jpg',
        title: '上海-名古屋 5天自由行',
        desc: '赠一晚酒店💕上海🛫名古屋5-7日自由行🎁代办签证代办签证代办签证代办签证代办签证代办签证'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/bb4e26c0-2d6b-43f4-a525-2b1e14875ae4.jpg_r_480x320x90_bbfe8901.jpg',
        title: '上海-名古屋 5天自由行',
        desc: '赠一晚酒店💕上海🛫名古屋5-7日自由行🎁代办签证代办签证代办签证代办签证代办签证代办签证'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top :.2rem
    line-height :.4rem
    background :#eee
    text-indent :2rem
   .item-img-wrapper
     height :0
     overflow :hidden
     padding-bottom :33.9%
   .item-img
     width :100%
   .item-info
     padding :.1rem

     .item-title
       line-height :.54rem
       font-size :.32rem
       ellipses()
     .item-desc
       line-height .4rem
       color :#ccc
       ellipses()
</style>
