<template>
  <el-header class="header">
    <img class="logo" src="@/assets/image/logo.jpg" alt="logo" />
  </el-header>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.header {
  height: 60px;
  width: 100%;
  border-bottom: 1px solid #000;
  box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.1);
  .logo {
    width: 240px;
    height: 100%;
  }
}
</style>
