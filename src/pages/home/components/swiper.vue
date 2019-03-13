<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl" alt=""></swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
        <!-- <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
        <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
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
        imgUrl: '//img1.qunarzz.com/vc/bf/9d/a3/67b7b37511fa26a78298bf1da1.jpg'
      },
      {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/vc/b8/25/51/f6173dbd12c1a0f783abe73855.jpg'
      },
      {
        id: '0003',
        imgUrl: '//img1.qunarzz.com/vc/a9/f4/f1/bb33ddb697f07c375e7af81256.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" socped>
.wrapper .swiper-pagination-bullet-active
  background #fff
  opacity 0.8
.wrapper
  width 100%
  overflow hidden
  height 0
  padding-bottom 31.25%
//   background #eeeeee
//height 31.25vw
  .swiper-img
    width 100%
</style>
