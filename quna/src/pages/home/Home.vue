<template>
  <div class="index-wrapper">
    <index-header :city="city"></index-header>
    <banner-carousel :swiper-imgs="swiperImgs"></banner-carousel>
    <category-nav :icon-list="iconList"></category-nav>
    <hot-list :rankList="rankList"></hot-list>
    <recommend :recommend-list="recommendList"></recommend>
    <go :weekend-list="weekendList"></go>
    <download-app class="download-app"></download-app>
  </div>
</template>

<script>
import IndexHeader from './components/Header'
import BannerCarousel from './components/BannerCarousel'
import CategoryNav from './components/CategoryNav'
import HotList from './components/HotLIst'
import Recommend from './components/Recommend'
import Go from './components/Go'
import DownloadApp from './components/DownloadApp'

export default {
  name: 'index',
  data () {
    return {
      city: '',
      swiperImgs: [],
      iconList: [],
      recommendList: [],
      weekendList: [],
      rankList: []
    }
  },
  components: {
    IndexHeader,
    BannerCarousel,
    CategoryNav,
    HotList,
    Recommend,
    Go,
    DownloadApp
  },
  mounted () {
    this.$axios.get('/api/index.json').then(
      res => {
        res = res.data
        if (res.ret && res.data) {
          let data = res.data
          this.city = data.city
          this.swiperImgs = data.swiperImgs
          this.iconList = data.iconList
          this.recommendList = data.recommendList
          this.weekendList = data.weekendList
          this.rankList = data.rankList
        }
      }
    )
  }
}
</script>

<style lang="stylus" scoped>
.index-wrapper
  background #f7f2f2
  height 100%
  overflow scroll
  .download-app
    height 1rem
    position: fixed
    left 0
    bottom 0
    z-index: 25;
</style>
