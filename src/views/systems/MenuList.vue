<template>
  <MainPanel>
    <div>{{ a }}</div>
    <el-button @click="add">加一</el-button>
  </MainPanel>
</template>
<script setup lang="ts">
const a = ref(0);
const add = () => {
  a.value += 1;
};
</script>
<style scoped></style>
