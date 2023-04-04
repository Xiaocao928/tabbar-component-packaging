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
  height: 50px;
  background-color: #f7f7f7;
  box-shadow: 0 0 10px 0 hsl(0deg 6% 58% / 60%);
}
</style>
