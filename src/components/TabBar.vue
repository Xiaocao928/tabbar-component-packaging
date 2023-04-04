<template>
  <div class="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBar',
  model: {
    prop: 'value',
    event: 'change',
  },
  props: {
    value: {
      type: Number,
      default: 0,
    },
  },
  watch: {
    value() {
      this.$children.forEach((item, index) => {
        item.active = index == this.value
      })
    },
  },
  mounted() {
    console.log(this.$children)
    // 在这个生命周期函数调用时, 所有的子组件tab-bar-item都已经挂载完成
    this.$children[this.value].active = true
  },
}
</script>

<style>
.tab-bar {
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 50px;
  background-color: #f7f7f7;
  box-shadow: 0 0 10px 0 hsl(0deg 6% 58% / 60%);
}
</style>
