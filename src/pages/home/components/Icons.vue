<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.imgUrl' />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      iconList: [
        {
          id: '0001',
          imgUrl: 'http://img.doutula.com/production/uploads/image/2019/03/13/20190313434056_FNTaHt.png',
          desc: '吃喝玩乐衣食住行'
        },
        {
          id: '0002',
          imgUrl: 'http://img.doutula.com/production/uploads/image/2019/03/13/20190313434057_BuQvSs.png',
          desc: '景点'
        },
        {
          id: '0003',
          imgUrl: 'http://img.doutula.com/production/uploads/image/2019/03/13/20190313434057_ZNsntG.png',
          desc: '景点'
        },
        {
          id: '0004',
          imgUrl: 'http://img.doutula.com/production/uploads/image/2019/03/13/20190313434058_HkKCUM.png',
          desc: '景点'
        },
        {
          id: '0005',
          imgUrl: 'https://ws2.sinaimg.cn/bmiddle/9150e4e5gy1g0r86xlg9yj201c01cgln.jpg',
          desc: '景点'
        },
        {
          id: '0006',
          imgUrl: 'https://ws3.sinaimg.cn/bmiddle/9150e4e5gy1g0r86z5mqoj201c01c0ss.jpg',
          desc: '景点'
        },
        {
          id: '0007',
          imgUrl: 'https://ws1.sinaimg.cn/bmiddle/9150e4e5gy1g0r870oy8bj201c01cdfv.jpg',
          desc: '景点'
        },
        {
          id: '0008',
          imgUrl: 'https://ws3.sinaimg.cn/bmiddle/9150e4e5gy1frctj9wf1ej201f01f0nx.jpg',
          desc: '景点'
        },
        {
          id: '0009',
          imgUrl: 'https://ws2.sinaimg.cn/bmiddle/9150e4e5gy1g10ulq8x0kj201f01bglg.jpg',
          desc: '景点'
        }
      ],
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      if (!this.iconList) {
        return
      }
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
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
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
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
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
