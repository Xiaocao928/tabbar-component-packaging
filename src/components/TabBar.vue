<template>
  <div class="tab-bar">
    <slot></slot>
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
</style>
