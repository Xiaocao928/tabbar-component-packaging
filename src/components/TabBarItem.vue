<template>
  <div :class="itemStyle" @click="handleClick">
    <i :class="iconStyle"></i>
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
      active: false,
    }
  },
  computed: {
    itemStyle() {
      return ['tab-bar-item', this.active ? 'current' : '']
    },
    iconStyle() {
      return ['iconfont', 'icon-' + this.icon]
    },
  },
  methods: {
    handleClick() {
      const index = this.$parent.$children.indexOf(this)
      this.$parent.$emit('change', index)
    },
  },
}
</script>

<style>
@import 'http://at.alicdn.com/t/c/font_3995085_9lst5ml09ag.css';
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
