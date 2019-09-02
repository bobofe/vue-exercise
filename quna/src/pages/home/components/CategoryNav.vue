<template>
  <swiper :options="swiperOption" >
    <swiper-slide v-for="(page,index) in pages" :key="index">
      <div class="category-nav-wrap">
        <div class="category-nav-item" v-for="item in page" :key="item.id">
          <img :src="item.imgSrc" alt="">
          <p>{{item.desciption}}</p>
        </div>
      </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
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
      pages: [],
      categoryList: [
        {
          id: '0',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desciption: '景点门票'
        },
        {
          id: '1',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          desciption: '故宫'
        },
        {
          id: '2',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desciption: '北京必游'
        },
        {
          id: '3',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
          desciption: '水上乐园'
        },
        {
          id: '4',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desciption: '一日游'
        },
        {
          id: '5',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
          desciption: '北水古镇'
        },
        {
          id: '6',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desciption: '动植物园'
        },
        {
          id: '7',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          desciption: '奥林匹克塔'
        },
        {
          id: '8',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          desciption: '奥林匹克塔'
        },
        {
          id: '9',
          imgSrc: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desciption: '动植物园'
        }
      ]
    }
  },
  methods: {
  },
  created () {
    this.pages = this.pageNum
    console.log(this.pages)
  },
  computed: {
    pageNum: function () {
      var pages = []
      var len = this.categoryList.length
      if (len > 8) {
        pages.push(this.categoryList.slice(0, 8))
        pages.push(this.categoryList.slice(8, this.categoryList.length))
        console.log(pages)
      } else {
        pages = this.categoryList
      }
      return pages
    }
  }
}

</script>

<style lang="stylus" scoped>
.swiper-container >>> .swiper-pagination-bullet
  width 0.1rem
  height 0.1rem
  border-radius 0.05rem
.swiper-container
  background: #fff
  margin-bottom .2rem
  .category-nav-wrap
    width 100%
    font-size 14px
    display flex
    flex-wrap wrap
    padding 0.2rem 0
    .category-nav-item
      width 25%
      text-align center
      img
        width 50%
      p
        padding 0.2rem 0.1rem
        overflow hidden
        text-overflow ellipsis
        white-space nowrap
</style>
