<demo>
基础用法
</demo>

<template>
<div>
  <Tabs v-model:selected="TabSelect">
    <Tab title="导航1">内容1</Tab>
    <Tab title="导航2">内容2</Tab>
    <Tab title="导航3">内容3</Tab>
  </Tabs>
</div>
</template>

<script lang="ts">
import Tabs from  '../../lib/Tabs.vue'
import Tab from  '../../lib/Tab.vue'
import {ref} from 'vue';
export default {
  components:{Tabs,Tab},
  setup(){
    const TabSelect =ref('导航1')
    return {TabSelect}
  }
}
</script>
