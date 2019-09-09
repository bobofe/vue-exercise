<template>
  <div class="header">
    <div class="back">
      <span class="arrow">
        <span class="arrow green"></span>
      </span>
    </div>
    <div class="search">
      <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="city">
        <span>{{this.currentCity}}</span><i class="arrow-top"></i>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: '',
  props: {
    city: String
  },
  computed: {
    currentCity: function () {
      return this.city
    }
  }
}
</script>

<style lang="stylus" scoped>
  /*@import "../../../assets/styles/variable.styl"*/
  /*@import "~@/assets/styles/variable.styl"*/
  @import "~styles/variable.styl"
  .header
    display flex
    height .8rem;
    line-height .8rem
    background $bgColor
    .back
      width 0.7rem
      margin-top 0.2rem
      .arrow
        position absolute
        border .2rem solid transparent
        border-right .2rem solid #ffffff
      .green
        border-right .2rem solid $bgColor
        left : -0.15rem
        top : -0.2rem
    .search
      padding-left 0.2rem
      color #eaeaea
      height 0.6rem
      line-height 0.6rem
      flex-grow 1
      margin 0.1rem  0
      background #ffffff
      border-radius 0.1rem
      span
        padding-right 0.15rem
    .city
      color #ffffff
      margin 0 0.2rem
      span
        display inline-block
        max-width 1.13rem
        overflow hidden
        white-space nowrap
      .arrow-top
        margin-left 0.1rem
        position relative
        border .15rem solid transparent
        border-top .15rem solid #ffffff
        top -0.05rem
</style>
