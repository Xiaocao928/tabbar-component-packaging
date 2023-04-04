<template>
  <div class="tab-bar-item">
    <i class="iconfont icon-cart"></i>
    {{ name }}
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
  props: {
    name: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
@import 'http://at.alicdn.com/t/c/font_3660333_clz5n3z0jtw.css';
.tab-bar-item {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
