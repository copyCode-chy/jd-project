<template>
  <!-- 顶部内容 -->
  <topbar></topbar>
  <div class="container">
    <div class="content">
      <!-- 头部内容 -->
      <headerBar></headerBar>

      <!-- 主要内容 -->
      <content></content>

      <!-- 商品列表 -->
      <goodsList></goodsList>

      <!-- 底部按钮 -->
      <bottom></bottom>

      <!-- 侧边栏目 -->
      <asideMenu class="aside"></asideMenu>
    </div>
  </div>
</template>

<script setup>
import topbar from './components/topbar.vue';
import headerBar from './components/headerBar.vue';
import content from './components/content.vue';
import goodsList from './components/goodsList.vue';
import bottom from './components/bottom.vue';
import asideMenu from './components/asideMenu.vue';
</script>

<style lang="scss" scoped src="../../assets/css/content-with.css"></style>

<style>
.container {
  background-color: rgb(247, 252, 253);
}

.aside {
  position: fixed;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}
</style>
