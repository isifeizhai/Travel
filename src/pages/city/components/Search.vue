<template>
    <div class="search">
        <span class="action"><input class="search-input" type="text" placeholder="输入城市名或拼音"></span>
    </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.search
  height .68rem
  padding 0  0.1rem
  background $bgColor
  .action
    display: block;
    position: relative;
    z-index: 2;
    height: .55rem;
    .search-input
      width 100%
      height 100%
      line-height .55rem
      text-align center
      border-radius .12rem
      border: 1px solid #dbe1e4;
      color #888
      font-size: .3rem;
      vertical-align: top;
      padding 0 0.1rem
      box-sizing border-box
</style>
