<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/df/df65113c1322333fa3.water.jpg_200x200_7b1b0027.jpg',
        title: '帝王大厦',
        desc: '人人都有一双发现美的眼睛'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1806/e7/e74b5f08f7c7ee9fa3.water.jpg_200x200_451e3e02.jpg',
        title: '西冲',
        desc: '深圳最美沙滩'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        title: '深圳野生动物园',
        desc: '亲子游玩好去处'
      }]
    } 
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      overflow hidden
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        margin-top .1rem
        line-height .3rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .2rem
        background #ff9300
        padding 0 .1rem
        border-radius .06rem
        color #fff
</style>
