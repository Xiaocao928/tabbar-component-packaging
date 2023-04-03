<template>
  <div class="tab-bar">
    <div class="tab-bar-item">首页</div>
    <div class="tab-bar-item">分类</div>
    <div class="tab-bar-item">购物车</div>
    <div class="tab-bar-item">我的</div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.tab-bar {
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 40px;
  background-color: pink;
}
.tab-bar-item {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
