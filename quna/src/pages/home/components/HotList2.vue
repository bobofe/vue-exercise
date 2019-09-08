<template>
  <div class="hotlist">
    <div class="hotlist-title">
      <h3>热门推荐</h3>
      <div class="all-lists">全部榜单</div>
    </div>
    <div class="hotlist-content">
      <ul class="hotlist-wrap">
        <li class="hotlist-item">
          <a href="">
            <div class="img-container">
              <img src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg" alt="">
            </div>
            <div>故宫</div>
            <div>￥60起</div>
          </a>
        </li>
        <li class="hotlist-item">
          <a href="">
            <div class="img-container">
              <img src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg" alt="">
            </div>
            <div>故宫</div>
            <div>￥60起</div>
          </a>
        </li>
        <li class="hotlist-item">
          <a href="">
            <div class="img-container">
              <img src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg" alt="">
            </div>
            <div>故宫</div>
            <div>￥60起</div>
          </a>
        </li>
        <li class="hotlist-item">
          <a href="">
            <div class="img-container">
              <img src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg" alt="">
            </div>
            <div>故宫</div>
            <div>￥60起</div>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data: function () {
    return {
    }
  }
}
</script>

<style lang="stylus" scoped>
.hotlist-title
  height 1rem
  line-height 1rem
  background: #cca
  overflow hidden
  padding 0 0.3rem
  h3
    float left
  .all-lists
    float right
.hotlist-content
  overflow scroll
  padding 0.2rem 0.3rem
  .hotlist-wrap
    width 16rem
    height
    .hotlist-item
      text-align center
      padding-right 0.1rem
      float left
      .img-container
        width 2rem
        height 0
        padding-bottom 2rem
        overflow hidden
        img
          width 100%
</style>
