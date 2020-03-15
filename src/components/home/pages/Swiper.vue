<template>
  <div class="wapper">
  <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for='item of swiperList' :key="item.id">
      <img class="swiper-img" :src='item.imgUrl'>
    </swiper-slide>

    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>

  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://imgs.qunarzz.com/vc/44/e9/86/95bc36c9e1c06ebd68bdfe222e.jpg_92.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://imgs.qunarzz.com/vc/6d/9f/35/b8ad5468f73fd60ec0ced086f6.jpg_92.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wapper>>>.swiper-pagination-bullet-active
    background :#fff
  .wapper
    width :100%
    height :0
    overflow: hidden
    padding-bottom :31.25%
    background #eee

    .swiper-img
      width :100%
</style>
