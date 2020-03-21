<template>
  <div>
  <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584778486517&di=e390c82ad06b8f4e58416b1b414ff1e9&imgtype=0&src=http%3A%2F%2Fmedia-cdn.tripadvisor.com%2Fmedia%2Fphoto-s%2F01%2F3e%2F05%2F40%2Fthe-sandbar-that-links.jpg"/>
    <div class="banner-info">
      <div class="banner-title">大连圣亚海洋世界（AAAA景区)</div>
      <div class="banner-number">
        <span class="iconfont banner-icon">&#xe63a;</span>39
      </div>
    </div>
  </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584778486517&di=9faaaccd968bcb540d0ec960778cc56b&imgtype=0&src=http%3A%2F%2Fmedia-cdn.tripadvisor.com%2Fmedia%2Fphoto-s%2F03%2Ff8%2F81%2F70%2Ftup-island.jpg',
        'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=1343015815,2335192405&fm=26&gp=0.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
.banner
  position :relative
  overflow :hidden
  height :0
  padding-bottom :55%
  .banner-img
    width :100%
  .banner-info
    display :flex
    position :absolute
    left :0
    right :0
    bottom :0
    line-height :.6rem
    color :#fff
    background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
    .banner-title
      font-size :.32rem
      padding :0 .2rem
      flex :1
    .banner-number
      margin-top :.14rem
      padding :0 .4rem
      height .32rem
      line-height :.32rem
      border-radius :.2rem
      background :$rgba(0,0,0,.8)
      font-size :.24rem
      .banner-icon
        font-size .24rem
</style>
