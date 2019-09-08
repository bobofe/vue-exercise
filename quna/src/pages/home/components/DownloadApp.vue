<template>
  <div class="fixed-wrapper">
    <div class="close">x</div>
    <div class="logo">
      <div class="foot-logo">
        <img class="" src="http://imgs.qunarzz.com/piao/fusion/1606/44/2605d5bd522e109a.png" alt="">
      </div>
    </div>
    <p class="info">使用去哪儿门票客户端<br>享受专属优惠体验更流畅</p>
    <a href="" class="app-download border">
      <div>立即下载</div>
    </a>
  </div>
</template>
<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/variable.styl"

.fixed-wrapper
  overflow hidden
  height .8rem
  width 100%
  background: rgba(0,0,0,.8)
  .close
    background: #ccc
    width .5rem
    height .5rem
    color #ffffff
    font-size .4rem
    border-radius 0 0 .4rem 0
    position absolute
    top 0
    left 0
    padding-left 0.1rem
    box-sizing border-box
  .logo
    float left
    padding-left .6rem
    height 1rem
    .foot-logo
      width .8rem
      height .8rem
      padding-top .1rem
      img
        width 100%
  .info
    float left
    color #ffffff
    padding-left .2rem
    position relative
    top 50%
    transform translateY(-50%)
    font-size .2rem
    line-height .3rem
  .app-download
    position relative
    top: 50%
    margin-top -.3rem
    margin-right .2rem
    float right
    width 2rem
    height .6rem
    text-align center
    line-height .6rem
    &:before
      border-color #25a4bb
      border-radius 10%
    &:after
      border-color #25a4bb
      border-radius 10%
</style>
