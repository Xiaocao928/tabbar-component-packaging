<template>
  <div class="tab-bar-item">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
}
</script>

<style>
.tab-bar-item {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
