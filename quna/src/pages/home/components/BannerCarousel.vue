<template>
    <div class="wrapper">
      <swiper :options="swiperOption" >
        <swiper-slide v-for="item in swiperImgsList" :key="item.id">
          <img class="swiper-img" :src="item.imgSrc" alt="">
        </swiper-slide>
        <!--      <div class="swiper-button-prev" slot="button-prev"></div>-->
        <!--      <div class="swiper-button-next" slot="button-next"></div>-->
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'bannerCarousel',
  props: {
    swiperImgs: Array
  },
  data: function () {
    return {
      swiperOption: {
        // 垂直切换
        // direction: 'vertical',
        // 是否循环播放
        loop: true,
        // 左右导航按钮
        prevButton: '.swiper-button-prev',
        nextButton: '.swiper-button-next',
        // 分页器
        pagination: '.swiper-pagination',
        paginationClickable: true,
        // 自动播放
        autoplay: 1000
      }
    }
  },
  computed: {
    swiperImgsList: function () {
      return this.swiperImgs
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
   // 穿透
  .wrapper >>> .swiper-pagination-bullet
    width 0.1rem
    height 0.1rem
  .wrapper
    background-color: #ffffff !important
    width 100%
    height 0
    padding-bottom 26.7%
    overflow hidden
    .swiper-img
      width 100%
</style>
