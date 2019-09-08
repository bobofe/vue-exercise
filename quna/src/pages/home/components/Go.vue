<template>
  <div class="weekend-wrapper">
    <h3 class="weekend-title">周末去哪</h3>
    <div class="item-list-content">
      <div class="item-list-item" v-for="item in weekendGoList" :key="item.id">
        <a href="">
          <div class="item-img">
            <img :src="item.imgUrl" :alt="item.title">
          </div>
          <div class="item-detail">
            <h4>{{item.title}}</h4>
            <p>{{item.desc}}</p>
          </div>
        </a>
      </div>
      <div class="tips">票面价是指通过景区指定窗口售卖的纸质门票上标注的价格</div>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
    }
  },
  props: {
    weekendList: Array
  },
  computed: {
    weekendGoList: function () {
      return this.weekendList
    }
  }
}
</script>

<style lang="stylus" scoped>
.weekend-wrapper
  margin-bottom 1rem
  font-size .28rem
  .weekend-title
    color #212121
    line-height 0.8rem
    padding-left 0.3rem
  .item-list-content
    .item-list-item
      background: #ffffff
      margin-bottom .1rem
      a
        color rgb(51, 51, 51)
        .item-img
          width 100%
          height 0
          padding-bottom 36.5%
          overflow hidden
          img
            width 100%
        .item-detail
          padding .3rem .2rem
          p
            font-size .2rem
            padding-top .15rem
            color #616161
            overflow hidden
            white-space nowrap
            text-overflow ellipsis
    .tips
      color #616161
      font-size: .28em;
      line-height: .5rem;
      padding-left .3rem
      background: #ffffff
</style>
