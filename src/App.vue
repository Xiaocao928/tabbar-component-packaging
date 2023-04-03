<template>
  <div id="app">
    <tab-bar>
      <!-- <div class="tab-bar-item">首页</div>
      <div class="tab-bar-item">分类</div>
      <div class="tab-bar-item">购物车</div>
      <div class="tab-bar-item">我的</div> -->
      <div class="tab-bar-item" v-for="tab in tabs" :key="tab.id">
        {{ tab.name }}
      </div>
    </tab-bar>
  </div>
</template>

<script>
//导入
import TabBar from './components/TabBar.vue'
export default {
  name: 'App',
  components: {
    TabBar,
  },
  data() {
    return {
      tabs: [
        { id: 1, name: '首页' },
        { id: 2, name: '分类' },
        { id: 3, name: '购物车' },
        { id: 4, name: '我的' },
      ],
    }
  },
}
</script>

<style></style>
