<template>
  <div id="app">
    <keep-alive>
      <component :is="views[active]"></component>
    </keep-alive>
    <zd-button>默认按钮</zd-button>
    <zd-button type="primary">主要按钮</zd-button>
    <zd-button type="success">成功按钮</zd-button>
    <tab-bar v-model="active">
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
import HomeView from './views/HomeView.vue'
import CateView from './views/CateView.vue'
import CartView from './views/CartView.vue'
import UserView from './views/UserView.vue'
import ZdButton from './components/ZDButton.vue'
export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem,
    HomeView,
    CateView,
    CartView,
    UserView,
    ZdButton,
  },
  data() {
    return {
      tabs: [
        { id: 1, name: '首页', icon: 'shouye' },
        { id: 2, name: '分类', icon: 'fenlei' },
        { id: 3, name: '购物车', icon: 'gouwuche' },
        { id: 4, name: '我的', icon: 'wode' },
      ],
      active: 0,
      views: ['HomeView', 'CateView', 'CartView', 'UserView'],
    }
  },
}
</script>

<style></style>
