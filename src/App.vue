<script setup lang="ts">
import zhCn from 'element-plus/lib/locale/lang/zh-cn';
import NavSilder from './components/layout/NavSilder.vue';
import TopHeader from './components/layout/TopHeader.vue';

const locale = zhCn;
</script>

<template>
  <el-container class="h-[100vh] flex-col">
    <TopHeader></TopHeader>
    <el-container class="flex">
      <NavSilder></NavSilder>
      <el-main class="flex-1 overflow-y-auto overflow-x-hidden p-0">
        <router-view></router-view>
      </el-main>
    </el-container>
  </el-container>

  <div class="container">
    <m-header></m-header>
    <m-content></m-content>
    <m-footer></m-footer>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
}
</style>
