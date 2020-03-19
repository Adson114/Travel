<template>
  <div>
  <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">
            {{item.title}}
          </p>
          <p class="item-desc">{{item.desc}}
          </p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1809/9d/f8db3b5cb0007702.jpg_r_390x260x95_4d32fd2d.jpg',
        title: '上海-名古屋 5天自由行',
        desc: '赠一晚酒店💕上海🛫名古屋5-7日自由行🎁代办签证代办签证代办签证代办签证代办签证代办签证'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1809/9d/f8db3b5cb0007702.jpg_r_390x260x95_4d32fd2d.jpg',
        title: '上海-名古屋 5天自由行',
        desc: '赠一晚酒店💕上海🛫名古屋5-7日自由行🎁代办签证代办签证代办签证代办签证代办签证代办签证'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1809/9d/f8db3b5cb0007702.jpg_r_390x260x95_4d32fd2d.jpg',
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
.item
  display : flex
  height :1.9rem
  overflow :hidden
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex :1
    padding :.1rem
    min-width :0
    .item-title
      line-height :.54rem
      font-size :.32rem
      ellipses()
    .item-desc
      line-height .4rem
      color :#ccc
      ellipses()
    .item-button
      line-height:.44rem
      margin-top :.16rem
      background :#ff9300
      padding :0 .2rem
      border-radius :.06rem
      margin-top :.2rem
      color :#fff
</style>
