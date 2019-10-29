<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.url" />
      </swiper-slide>
      <!-- 滚动条下面的几个小点 -->
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
      <!-- 左右箭头 -->
      <!-- <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div> -->
      <!-- 下面滚动条 -->
      <!-- <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'homeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', // 使用小圆点分页
        loop: true// 支持无缝衔接
      },
      swiperList: [
        {
          id: '001',
          url: 'http://img1.qunarzz.com/piao/fusion/1803/98/0a2e0bd8eb0c0802.png_750x200_0a34d4a8.png'
        },
        {
          id: '002',
          url: 'http://img1.qunarzz.com/piao/fusion/1809/3e/52e1824f1ace7202.jpg_750x200_ac90db3f.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
//   加上scoped使得style的样式只在当前页面中有效,
//   而swiper是引入到了当前页面,但是swiper-slide还是其他页面内容
//   使用>>>实现样式穿透,使得swiper下组件只要出现了swiper-pagination-bullet-active这个样式,就采取相应效果
  .swiper >>> .swiper-pagination-bullet-active
    background: #fff!important;
  .swiper
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.67%;
    background-color: #ccc;
    .swiper-img
      width: 100%;
</style>
