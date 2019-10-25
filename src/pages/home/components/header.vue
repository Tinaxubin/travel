<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont icon-back">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市\景点\旅游主题</div>
    <div class="header-right">城市
      <span class="iconfont icon-select">&#xe615;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'homeHeader'
}
</script>

<!-- 用scoped实现当前样式只在当前页面使用 -->
<style lang="stylus" scoped>
  @import '~style/verible.styl'
  .header
  // 1rem=px/50，而页面设计都是2倍，所以除100
    line-height: .86rem;
    display: flex;
    background-color: $bgColor;
    color: #fff;
    .header-left
      width: .64rem;
      float: left;
      .icon-back
        display: inline-block;
        width: 100%;
        text-align: center;
    .header-input
      flex: 1;
      height: .62rem;
      line-height: .62rem;
      margin-top: .12rem;
      margin-left: .2rem;
      padding-left: .2rem;
      background-color: #fff;
      border-radius: .1rem;
      color: #ccc;
    .header-right
      width: 1.24rem;
      float: right;
      text-align: center;
      .icon-select {
        font-size: .2rem;
        margin-left: -.04rem;
      }
</style>
