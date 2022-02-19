<template>
  <div>
    <h1>#Dialog示例</h1>
    <section class="first-section">
      <h2><span>#</span>基础用法</h2>
      <p>使用<span>v-model</span>来绑定一个<span>Boolean</span>类型的变量到<span>Dialog</span>组件</p>
      <Demo :component="DialogNormal"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持closeOnClockOverlay</h2>
      <p>使用<span>closeOnClockOverlay</span>来控制<span>Dialog</span>能否通过点击<span>遮罩层</span>来关闭组件</p>
      <Demo :component="DialogClose"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持自定义title</h2>
      <p>在<span>Dialog</span>组件中添加<span>title</span>来编辑<span>Dialog</span>组件的标题</p>
      <Demo :component="DialogTitle"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>一键打开Dialog</h2>
      <p>使用<span>openDialog</span>模块来创建一个<span>Dialog</span>组件</p>
      <Demo :component="DialogOpen"/>
    </section>
  </div>
  <div class="next">
    <router-link to="/doc/button">上一节：Button组件</router-link>
    <router-link to="/doc/tabs">下一节：Tabs组件</router-link>
  </div>
</template>


<script lang="ts">
import Demo from  './Demo.vue'
import Dialog from '../lib/Dialog.vue';
import Button from '../lib/Button.vue';
import DialogNormal from './DialogComponents/DialogNormal.vue'
import DialogClose from './DialogComponents/DialogClose.vue'
import DialogTitle from './DialogComponents/DialogTitleAndContent.vue'
import DialogOpen from './DialogComponents/DialogOpen.vue'
export default {
  components: {Dialog, Button,Demo},
  setup() {
    return {DialogNormal,DialogClose,DialogTitle,DialogOpen};
  },
};
</script>


<style lang="scss" scoped>
span{
  color: red;
  line-height: 2;
}
.next{
  display: flex;
  justify-content: space-between;
}
</style>

