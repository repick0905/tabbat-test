<template>
  <div id="app">
    <router-view></router-view>
    <tab-bar>
      <tab-bar-item path="/home">
        <img src="../public/img/icons/Home.svg" alt slot="item-icon" />
        <img src="../public/img/icons/Home-click.svg" alt slot="item-icon-click" />
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category">
        <img src="../public/img/icons/App.svg" alt slot="item-icon" />
        <img src="../public/img/icons/App-click.svg" alt slot="item-icon-click" />
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/shopping">
        <img src="../public/img/icons/Shopping.svg" alt slot="item-icon" />
        <img src="../public/img/icons/Shopping-click.svg" alt slot="item-icon-click" />
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile">
        <img src="../public/img/icons/Person.svg" alt slot="item-icon" />
        <img src="../public/img/icons/Person-click.svg" alt slot="item-icon-click" />
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "@/components/tabbar/TabBar";
import TabBarItem from "@/components/tabbar/TabBarItem";

export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem
  }
};
</script>

<style>
</style>
