<template>
<!-- 分组图书样式 -->
  <div class="shelf-item-category">
    <div class="shelf-item-category-list">
      <div class="shelf-item-category-item" v-for="(item, index) in data.itemList" :key="index">
        <img :src="item.cover" alt="" class="shelf-item-category-img">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object
  }
}
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
@import "../../assets/styles/global";
.shelf-item-category{
  width: 100%;
  height: 100%;
  overflow: hidden;
  .shelf-item-category-list{
    display: flex;
    flex-flow: row wrap;
    width: 100%;
    height: 100%;
    .shelf-item-category-item{
      width: 33.33%;
      flex: 0 0 33.33%;
      height: 33.33%;
      box-sizing: border-box;
      &:nth-child(3n+1) {
        padding: px2rem(0) px2rem(2.5) px2rem(5) px2rem(5);
      }
      &:nth-child(3n+2) {
        padding: px2rem(0) px2rem(2.5) px2rem(5) px2rem(2.5);
      }
      &:nth-child(3n+3) {
        padding: px2rem(0) px2rem(5) px2rem(5) px2rem(2.5);
      }
      &:nth-child(-n+3) {
        padding-top: px2rem(5);
      }
      .shelf-item-category-img{
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>
