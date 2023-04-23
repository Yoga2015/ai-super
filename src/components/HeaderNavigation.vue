<script lang="ts" setup>
import { ref } from 'vue'

const activeIndex = ref('1')
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<template>
  <div id="HeaderNavigation" style=" width: 100%; display: flex; justify-content: space-between; max-width: 1280px;">

    <!-- logo图片 -->
    <div>
      <img src="../assets/logo.svg" alt="图片" width="65" height="65">
    </div>

    <!-- 菜单 -->
    <div style="display: flex; justify-content: space-between; align-items: center;">
      <div>
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :ellipsis="false"
          @select="handleSelect">
          <div class="flex-grow" />
          <el-menu-item index="1">🔥Trending</el-menu-item>
          <el-menu-item index="2">✨Recently Added</el-menu-item>
          <el-menu-item index="3">🎁Get Deals</el-menu-item>
        </el-menu>
      </div>

      <div style="display: flex; justify-content: space-evenly;">
        <el-button type="primary" size="large">Submit a tool</el-button>
      </div>
    </div>

  </div>
</template>

<style scoped>
.flex-grow {
  flex-grow: 1;
}
</style>
