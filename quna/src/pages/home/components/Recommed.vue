<template>
  <div class="recommend-wrapper">
    <h3 class="recommend-title">猜你喜欢</h3>
    <div class="like-list">
      <div class="like-list-item" v-for="item in lovedList" :key="item.id">
        <div class="like-img">
          <img :src="item.imgSrc" :alt="item.title">
        </div>
        <div class="like-detail">
          <h4>{{item.title}}</h4>
          <p class="rate"><span class="iconfont "></span><span>{{item.reviewNum}}</span>条评论</p>
          <div class="clearfix">
            <div class="price"><span class="rmb">￥</span><span class="price-num">{{item.price}}</span>起</div>
            <div class="location">{{item.location}}</div>
          </div>
          <div class="description" v-if="item.show">{{item.description}}</div>
        </div>
      </div>
      <div class="get-all">查看所有产品</div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data: function () {
    return {
      mes: '',
      showDetail: 'false',
      lovedList: [
        {
          id: '0',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
          title: '北京欢乐谷',
          rate: '',
          reviewNum: '75068',
          price: '195',
          location: '朝阳区',
          description: '亚洲唯一飞行式过山车等你来挑战'
        },
        {
          id: '1',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
          title: '北京欢乐谷',
          rate: '',
          reviewNum: '75068',
          price: '195',
          location: '朝阳区',
          description: ''
        },
        {
          id: '2',
          imgSrc: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
          title: '北京欢乐谷',
          rate: '',
          reviewNum: '75068',
          price: '195',
          location: '朝阳区',
          description: '亚洲唯一飞行式过山车等你来挑战'
        }
      ]
    }
  },
  created () {
    this.judgeDes()
  },
  methods: {
    judgeDes: function () {
      this.lovedList.forEach(function (item) {
        if (item.description !== '') {
          item['show'] = true
        } else {
          item['show'] = false
        }
      })
      console.log(this.lovedList)
    }
  },
  computed: {
  }
}
</script>

<style lang="stylus" scoped>
.recommend-wrapper
  padding 0.3rem
  padding-bottom 0
  background: #fff
  .recommend-title
    font-size .35rem
    font-weight bold
    padding-bottom  0.3rem
  .like-list-item
    border-bottom 1px solid #ccc
    padding 0.2rem 0
    display flex
    flex-wrap wrap
    .like-img
      width 2rem
      margin-right 0.34rem
      img
        width 2rem
        height 2rem
    .like-detail
      flex-grow 1
      h4
        line-height .8rem
        font-size .36rem
      .rate
        font-size 0.14rem
        padding-bottom  .2rem
      .clearfix
        overflow hidden
        display flex
        justify-content space-between
        .price
          .rmb
            color red
            font-size .14rem
          .price-num
            font-size .4rem
            color red
        .location
          padding-top .15rem
          font-size .16rem
      .description
        padding  0.6rem 0 0.1rem
        color: red
        font-size 0.14rem
  .get-all
    color: #49C2D4
    text-align center
    font-size .3rem
    line-height .8rem
</style>
