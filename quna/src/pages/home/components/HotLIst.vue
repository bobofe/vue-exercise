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
        <div class="rank-list-item" v-for="item in hotRankList" :key="item.id">
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
      mes: ''

    }
  },
  props: {
    rankList: Array
  },
  components: {},
  methods: {},
  computed: {
    hotRankList: function () {
      return this.rankList
    }
  },
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
