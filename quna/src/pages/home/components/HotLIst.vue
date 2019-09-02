<template>
  <div class="hot-list">
    <div class="hot-list-header">
      <h3 class="hot-list-title">本周热门榜单</h3>
      <div class="all-list">
        全部榜单
        <div class="all">
          <span class="arrow">
            <span class="arrow green"></span>
          </span>
        </div>
      </div>
    </div>
    <div class="scroll-bar">
      <div class="rank-list-wrapper">
        <div class="rank-list-item" v-for="item in rankList" :key="item.id">
          <img :src="item.imgSrc" :alt="item.name">
          <p>{{item.name}}</p>
          <p><span>￥{{item.price}}</span>起</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data: function () {
    return {
      mes: '',
      rankList: [
        {
          id: '0',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
          name: '故宫',
          price: '60'
        },
        {
          id: '1',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_250x250_50c99cf3.jpg',
          name: '八达岭长城',
          price: '40'
        },
        {
          id: '2',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_250x250_d852635b.jpg',
          name: '颐和园',
          price: '36'
        },
        {
          id: '3',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_250x250_63e3520a.jpg',
          name: '圆明园',
          price: '25'
        },
        {
          id: '4',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/201405/12/51b63883c25f5d87af3c08bb016e2bd7.jpg_250x250_6ec2f798.jpg',
          name: '恭王府',
          price: '28.8'
        },
        {
          id: '5',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1602/92/920e47352552c1c990.water.jpg_250x250_ee99c18e.jpg',
          name: '天坛公园',
          price: '40'
        },
        {
          id: '6',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_250x250_6c4c9885.jpg',
          name: '北京欢乐谷',
          price: '195'
        },
        {
          id: '7',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_250x250_3588bc9a.jpg',
          name: '北京世界园艺博览',
          price: '108'
        },
        {
          id: '8',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_250x250_d76e727c.jpg',
          name: '北京动物园',
          price: '175'
        },
        {
          id: '9',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_250x250_ecfa0df2.jpg',
          name: '水立方',
          price: '248'
        }
      ]
    }
  },
  components: {},
  methods: {},
  computed: {},
  created () {
  }
}
</script>

<style lang="stylus" scoped>
  .hot-list
    background: #fff
    margin-bottom 0.2rem
    .hot-list-header
      padding 0.3rem 0.6rem 0.3rem 0.3rem
      display flex
      justify-content space-between
      .hot-list-title
        font-size .35rem
        font-weight bold
      .all-list
        color #aaa
        .all
          position relative
          float: right
          right -0.1rem
          top: -.3rem
          .arrow
            position absolute
            border .14rem solid transparent
            border-left .14rem solid #aaa
            .green
              border-left .14rem solid #ffffff
              left : -0.19rem
              top : -0.14rem
    .scroll-bar
      width 100%
      white-space nowrap
      overflow-x scroll
      padding-bottom 0.2rem
      .rank-list-wrapper
        width 21rem
        display flex
        flex-wrap nowrap
        padding 0 0.25rem
        white-space nowrap
        .rank-list-item
          padding 0 .05rem
          text-align center
          font-size 0.12rem
          img
            width 2rem
            height 2rem
          p
            padding-top 0.15rem
            span
              color #FDC99E
              font-size .25rem
</style>
