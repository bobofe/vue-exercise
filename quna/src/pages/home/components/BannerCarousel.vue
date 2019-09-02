<template>
    <div class="wrapper">
      <swiper :options="swiperOption" >
        <swiper-slide v-for="item in swiperImgs" :key="item.id">
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
  data: function () {
    return {
      swiperImgs: [
        {
          id: '0',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
        },
        {
          id: '1',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg'
        },
        {
          id: '2',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/eb3fdb7ff86de0160cafe76b6a6a8ee3.jpg_750x200_e6930e5c.jpg'
        },
        {
          id: '3',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/0b0622e5b6ac5fbed3084dd2832e6f8f.jpg_750x200_895321b6.jpg'
        },
        {
          id: '4',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/279640fb8c1f7eea398045bfe8ac92b1.png_750x200_ac53465f.png'
        },
        {
          id: '5',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/06e65ace8dce3638e847b04e975489d1.jpg_750x200_a2dcb0a4.jpg'
        },
        {
          id: '6',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/2df3ba0f23801d7ed5607f4767a18482.jpg_750x200_b4d6aa93.jpg'
        },
        {
          id: '7',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/a4c27b0a5fc1d9e9e620225869089b12.jpg_750x200_e4720428.jpg'
        },
        {
          id: '8',
          imgSrc: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/fffc0c06ddfe6fa9bad3cd813b591873.jpg_750x200_528c2db7.jpg'
        }
      ],
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
