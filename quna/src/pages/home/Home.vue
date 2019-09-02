<template>
  <div class="index-wrapper">
    <index-header></index-header>
    <banner-carousel></banner-carousel>
    <category-nav></category-nav>
    <hot-list></hot-list>
    <recommed></recommed>
  </div>
</template>

<script>
import IndexHeader from './components/Header'
import BannerCarousel from './components/BannerCarousel'
import CategoryNav from './components/CategoryNav'
import HotList from './components/HotLIst'
import Recommed from './components/Recommed'

export default {
  name: 'index',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    IndexHeader,
    BannerCarousel,
    CategoryNav,
    HotList,
    Recommed
  }
}
</script>

<style lang="stylus" scoped>
.index-wrapper
  background #f7f2f2
</style>
