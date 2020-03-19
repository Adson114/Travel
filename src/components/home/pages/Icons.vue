<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page ,index) of pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content"
                 :src="item.imgUrl"/>
          </div>
          <p class="icon-desc"> {{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '001',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584589814636&di=9c8000e729c3f4f6c667f8ac6d93359e&imgtype=0&src=http%3A%2F%2Fbpic.588ku.com%2Felement_origin_min_pic%2F01%2F34%2F24%2F46573ba46374d72.jpg',
        desc: '景点门票'
      }, {
        id: '002',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584591162408&di=a7eb78c8babfe30a361158754d7d1191&imgtype=0&src=http%3A%2F%2Fpic.51yuansu.com%2Fpic2%2Fcover%2F00%2F46%2F28%2F58156e7d6230a_610.jpg',
        desc: '滑雪季节'
      }, {
        id: '003',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584591244306&di=e00d83ed724940eb7810af6c7883e3c0&imgtype=0&src=http%3A%2F%2Fimg.jpshopguide.com%2FS2700%2Fupload%2F2017022704236_1.jpg',
        desc: '泡温泉'
      }, {
        id: '004',
        imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3650627178,2047022812&fm=15&gp=0.jpg',
        desc: '动植物园'
      }, {
        id: '005',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584589814636&di=9c8000e729c3f4f6c667f8ac6d93359e&imgtype=0&src=http%3A%2F%2Fbpic.588ku.com%2Felement_origin_min_pic%2F01%2F34%2F24%2F46573ba46374d72.jpg',
        desc: '景点门票'
      }, {
        id: '006',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584591162408&di=a7eb78c8babfe30a361158754d7d1191&imgtype=0&src=http%3A%2F%2Fpic.51yuansu.com%2Fpic2%2Fcover%2F00%2F46%2F28%2F58156e7d6230a_610.jpg',
        desc: '滑雪季节'
      }, {
        id: '007',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1584591244306&di=e00d83ed724940eb7810af6c7883e3c0&imgtype=0&src=http%3A%2F%2Fimg.jpshopguide.com%2FS2700%2Fupload%2F2017022704236_1.jpg',
        desc: '泡温泉'
      }, {
        id: '008',
        imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3650627178,2047022812&fm=15&gp=0.jpg',
        desc: '动植物园'
      }, {
        id: '009',
        imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3650627178,2047022812&fm=15&gp=0.jpg',
        desc: '一日游'
      }]
    }
  },
  computed: {

    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor((index / 8))
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
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"

  .icons>>>.swiper-container
    height: 0
    padding-bottom 50%
  .icons
    margin-top :.1rem
   .icon
     position: relative
     overflow: hidden
     width: 25%
     height: 0
     float: left
     padding-bottom: 25%

     .icon-img
       position: absolute
       top: 0
       left: 0
       right: 0
       bottom: .44rem
       box-sizing: border-box
       padding: .1rem

       .icon-img-content
         display: block
         margin: 0 auto
         width: 100%
         height: 100%

     .icon-desc
       position: absolute
       left: 0
       right: 0
       bottom: 0
       height .44rem
       line-height .44rem
       color: $darkTextColor
       ellipses()
</style>
