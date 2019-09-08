<template>
  <div class="category-wrapper">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <!--   外层的包裹   -->
        <div class="category-nav-wrap">
          <!-- 单块 -->
          <div class="category-nav-item" v-for="item in page" :key="item.id">
            <img :src="item.imgUrl" alt="">
            <p>{{item.desc}}</p>
          </div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    <div class="nav-item border-top">
      <span>定位失败</span><i class="divided border-right"></i><span>必游榜单</span>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data: function () {
    return {
      swiperOption: {
        // 分页器
        pagination: '.swiper-pagination',
        paginationClickable: true
      },
      pages: []
    }
  },
  props: {
    iconList: Array
  },
  created () {
    this.pages = this.pageNum
    console.log(this.pages)
  },
  computed: {
    cateIconList: function () {
      return this.iconList
    },
    pageNum: function () {
      var pages = []
      var len = this.cateIconList.length
      if (len > 8) {
        pages.push(this.cateIconList.slice(0, 8))
        pages.push(this.cateIconList.slice(8, this.cateIconList.length))
        console.log(pages)
      } else {
        pages = [...this.cateIconList]
      }
      return pages
    }
  }
}

</script>

<style lang="stylus" scoped>
@import "~styles/variable.styl"

.category-wrapper >>> .swiper-pagination-bullet-active
  background $bgColor
.category-wrapper >>> .swiper-pagination-bullet
  width 0.1rem
  height 0.1rem
  border-radius 0.05rem
.swiper-container
  background: #fff
  .category-nav-wrap
    width 100%
    font-size 14px
    display flex
    flex-wrap wrap
    // 利用padding的布局不好，如果图纸给的是2：1的比例，不可能去这样算，最好通过布局一步到位，而不是这样算
    // padding和margin的数值属性值适合微调，不适合拿来布局
    padding 0.2rem 0
    .category-nav-item
      width 25%
      text-align center
      img
        width 1.1rem
      p
        padding 0.2rem 0.1rem
        overflow hidden
        text-overflow ellipsis
        white-space nowrap
.nav-item
  height 1rem
  line-height 1rem
  text-align center
  background: #ffffff
  margin-bottom 0.2rem
  display flex
  &:before
    background: #ccd
  span
    flex-grow 1
  .divided
    &:before
      background #ccd
</style>
