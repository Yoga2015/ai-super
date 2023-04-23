<script setup lang="ts">
import { ref } from 'vue'
import { Search } from '@element-plus/icons-vue'

const input = ref('')
const value = ref('')
const options = [
  {
    value: 'Freemium',
    label: 'Freemium',
  },
  {
    value: 'Free',
    label: 'Free',
  },
  {
    value: 'Paid',
    label: 'Paid',
  },
]

</script>

<template>
  <div style="width: 100%; padding-bottom: 2%;">

    <div style="display: flex; justify-content: space-around;">
      <el-text type="primary" style="font-size: 1.875rem;">
        Find Best AI Tools That Make Your Life Easy!
      </el-text>
    </div>

    <div style="display: flex; justify-content: center; padding: 2%;">
      <div>
        <el-input v-model="input" size="large" placeholder="Please input" :prefix-icon="Search" style="width: 500px" />
        <el-button type="primary" size="large" placeholder="Please Input">Search</el-button>
      </div>
      <div style="padding-left: 2%;">
        <el-select v-model="value" size="large" placeholder="All">
          <el-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value" />
        </el-select>
      </div>
    </div>

    <div>
      <div style="display: flex; justify-content: space-around;">
        <div>
          <a href="javascript:;"><span>Copywriting</span></a>
          <a href="javascript:;"><span>Content Creation</span></a>
          <a href="javascript:;"><span>Image Generation</span></a>
          <a href="javascript:;"><span>Productivity</span></a>
          <a href="javascript:;"><span>Writing Assistant</span></a>
          <a href="javascript:;"><span>Video Generation</span></a>
          <a href="javascript:;"><span>Design</span></a>
          <a href="javascript:;"><span>Video Editing</span></a>
          <a href="javascript:;"><span>Audio Generation</span></a>
          <a href="javascript:;"><span>Chat Bot</span></a>
        </div>
      </div>
      <div style="display: flex; justify-content: space-around;">
        ...and more
      </div>
    </div>


  </div>
</template>

<style scoped>
a {
  padding-right: 15px;
  color: #409EFF;
}
</style>