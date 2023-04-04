<template>
  <div id="app">
    <tab-bar>
      <!-- <div class="tab-bar-item">首页</div>
      <div class="tab-bar-item">分类</div>
      <div class="tab-bar-item">购物车</div>
      <div class="tab-bar-item">我的</div> -->
      <tab-bar-item v-for="tab in tabs" :key="tab.id" :icon="tab.icon">
        {{ tab.name }}
      </tab-bar-item>
      <!-- <tab-bar-item icon="home">首页</tab-bar-item>
      <tab-bar-item icon="category">分类</tab-bar-item>
      <tab-bar-item icon="cart">购物差</tab-bar-item>
      <tab-bar-item icon="user">我的</tab-bar-item> -->
    </tab-bar>
  </div>
</template>

<script>
//导入
import TabBar from './components/TabBar.vue'
import TabBarItem from './components/TabBarItem.vue'
export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem,
  },
  data() {
    return {
      tabs: [
        { id: 1, name: '首页', icon: 'home' },
        { id: 2, name: '分类', icon: 'category' },
        { id: 3, name: '购物车', icon: 'cart' },
        { id: 4, name: '我的', icon: 'user' },
      ],
    }
  },
}
</script>

<style></style>
