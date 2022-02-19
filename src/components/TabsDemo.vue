<template>
  <h1>#Tabs示例</h1>
  <section class="first-section">
    <h2><span>#</span>基础用法</h2>
    <p>使用<span>v-model</span>来绑定一个<span>Boolean</span>类型的变量到<span>Tabs</span>组件</p>
    <Demo :component="TabNormal"/>
  </section>
  <div class="next">
    <router-link to="/doc/dialog">上一节：Dialog组件</router-link>
  </div>
</template>


<script lang="ts">
import Demo from './Demo.vue'
import TabNormal from './TabComponents/TabNormal.vue'
export default {
  components:{Demo},
  setup(){
    return {TabNormal}
  }
}

</script>

<style lang="scss" scoped>
span {
  color: red;
  line-height: 2;
}
</style>

