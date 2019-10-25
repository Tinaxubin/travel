<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide>
        <img class="swiper-img" src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1572021318012&di=072f59b39902993a041624aeff868fe9&imgtype=0&src=http%3A%2F%2Fp4-q.mafengwo.net%2Fs9%2FM00%2FBC%2F91%2FwKgBs1b7e9SANgXsADNR-a5p1tw97.jpeg"/>
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1572021497104&di=152bcbb802e0ceae4dfdd698504d9051&imgtype=jpg&src=http%3A%2F%2Fimg3.imgtn.bdimg.com%2Fit%2Fu%3D2055447958%2C3298526593%26fm%3D214%26gp%3D0.jpg"/>
      </swiper-slide>
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
    name: "homeSwiper",
    data() {
      return{
        swiperOption: {}
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .swiper
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 31.25%;
    background-color: #ccc;
    .swiper-img
      width: 100%;
</style>
