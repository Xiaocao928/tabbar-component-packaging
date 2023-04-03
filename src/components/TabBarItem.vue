<template>
  <div class="tab-bar-item">
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
.tab-bar-item {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
