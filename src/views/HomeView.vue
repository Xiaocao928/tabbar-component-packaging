<template>
  <div>
    首页
    <div>
      <button @click="handleClick">点击{{ count }}次</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      count: 0,
    }
  },
  methods: {
    handleClick() {
      this.count++
    },
  },
}
</script>

<style></style>
