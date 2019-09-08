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

</script>

<style lang="stylus" scoped>
</style>
