<template>
    <div>
        <div class="title"> 热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl" alt="">
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
          title: '故宫',
          desc: '还记得影视剧中，皇帝上朝的金銮殿嘛？金銮殿名为太和殿，是皇帝登基和举行大典的地方。'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/fe/434ee530e21f1c11bad088e8cc8d5e93.water.jpg_200x200_912ce9f4.jpg',
          title: '鸟巢',
          desc: '北京奥运会期间，鸟巢作为主会场，承担开闭幕式、田径赛事和足球决赛。精彩绝伦的表演与大气宏伟结构相得益彰，令世人惊艳。'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/5d/5dcaf453dfd6f5dba3.img.jpg_200x200_51d03f19.jpg',
          title: '古水北镇',
          desc: '永顺染，草木色，手工缬，天然彩”。观赏原汁原味的生态印染。老师手把手教你DIY属于自己的印染作品。'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1604/1e/1e75f8e1af9fe81f90.img.jpg_200x200_0ded2b1b.jpg',
          title: '世界花卉大观园',
          desc: '世界花卉大观园一期景观由七大温室和十五个花园广场组成。精品花卉温室展示了各国名优花卉品种和植物造型盆景，其中还增加了一些古船、战车、水车等古老的设施。'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eeeeee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      min-width 0
      flex 1
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color rgb(255, 85, 85)
        ellipsis()
      .item-button
        line-height .05rem
        background #ff9300
        padding 0.2rem
        border-radius .1rem
        margin-top .06rem
        color #fff
</style>
