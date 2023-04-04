<template>
  <button :class="btnStyle">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'ZdButton',
  props: {
    type: String,
    default: '',
  },
  computed: {
    btnStyle() {
      return {
        'zd-button': true,
        'zd-button--primary': this.type === 'primary',
        'zd-button--success': this.type === 'success',
      }
    },
  },
}
</script>

<style scoped>
/* scoped,将css样式限定到当前组件 */
.zd-button {
  margin: 0 5px;
  padding: 12px 20px;
  font-size: 14px;
  border: 1px solid #dcdfe6;
  color: #606266;
  white-space: nowrap;
  cursor: pointer;
  box-sizing: border-box;
  border-radius: 4px;
  transition: 0.1s;
  font-size: 500;
}
.zd-button:hover {
  color: #409eff;
  border-color: #c6e2ff;
  background-color: #ecf5ff;
}
.zd-button--primary {
  color: #fff;
  background-color: #409eff;
  border-color: #409eff;
}
.zd-button--primary:hover {
  background: #66b1ff;
  border-color: #66b1ff;
  color: #fff;
}
.zd-button--success {
  color: #fff;
  background-color: #67c23a;
  border-color: #67c23a;
}
.zd-button--success:hover {
  background: #85ce61;
  border-color: #85ce61;
  color: #fff;
}
</style>
