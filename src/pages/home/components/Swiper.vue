<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
        <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/a4be7d0dc88a518dd5217c16156023d9.jpg_890x330_59f02d53.jpg'
      },{
        id: '0002',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/2c40f50f55e2026f0d42f89df97bd3d2.jpg_890x330_5197528c.jpg'
      },]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active 
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 37.07%
    background #eee
    .swiper-img
        width: 100%
</style>
