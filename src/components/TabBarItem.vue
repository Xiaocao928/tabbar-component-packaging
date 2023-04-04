<template>
  <div :class="['tab-bar-item', active ? 'current' : '']">
    <i :class="['iconfont', 'icon-' + icon]"></i>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
  props: {
    icon: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      active: true,
    }
  },
}
</script>

<style>
@import 'http://at.alicdn.com/t/c/font_3660333_clz5n3z0jtw.css';
.tab-bar-item {
  flex: 1;
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
  color: #666;
}
.tab-bar-item i {
  font-size: 18px;
}
.tab-bar .current {
  color: #e93b3b;
}
</style>
