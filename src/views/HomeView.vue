<script setup lang="ts">
import ToolSearch from '../components/ToolSearch.vue'
import ToolList from '../components/ToolList.vue'
import MyFooter from '@/components/MyFooter.vue';

</script>

<template>
  <main>
    <div>
      <div>
        <ToolSearch />
      </div>
      <div>
        <ToolList />
      </div>

      <MyFooter />
    </div>

  </main>
</template>
