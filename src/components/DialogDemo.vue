<template>
  <div>
    <h1>#Dialog示例</h1>
    <section class="first-section">
      <h2><span>#</span>基础用法</h2>
      <p>使用<span>v-model</span>来绑定一个<span>Boolean</span>类型的变量到<span>Dialog</span>组件</p>
      <Demo :component="DialogNormal"/>
    </section>
<!--    <section class="first-section">-->
<!--      <h2><span>#</span>支持closeOnClickOverlay</h2>-->
<!--      <p>使用<span>closeOnClickOverlay</span>来控制<span>Dialog</span>组件能否通过遮罩层来关闭<span>Dialog</span>组件</p>-->
<!--      <Demo :component="DialogClose"/>-->
<!--    </section>-->

    <h1>示例1</h1>
    <Button @click="toggle">toggle</Button>
    <Dialog v-model:visible="x" :closeOnClickOverlay="false" :ok="f1" :cancel="f2">
      <template v-slot:content>
        <div>你好</div>
        <div>hi</div>
      </template>
      <template v-slot:title>
        <div>自定义标题</div>
      </template>
    </Dialog>
    <h1>示例2</h1>
    <Button @click="showDialog">show</Button>
  </div>
</template>


<script lang="ts">
import Demo from  './Demo.vue'
import Dialog from '../lib/Dialog.vue';
import Button from '../lib/Button.vue';
import {ref} from 'vue';
import {openDialog} from '../lib/openDialog.ts';
import DialogNormal from './DialogComponents/DialogNormal.vue'
import DialogClose from './DialogComponents/DialogClose.vue'
export default {
  components: {Dialog, Button,Demo},
  setup() {
    const x = ref(false);
    const toggle = () => {
      x.value = !x.value;
    };
    const f1 = () => {
      return false;
    };
    const f2 = () => {
    };
    const showDialog = () => {
      openDialog({title:'标题',content:'你好'})
    };
    return {showDialog, toggle,DialogNormal,DialogClose,f1, f2,};
  },
};
</script>


<style lang="scss" scoped>
span{
  color: red;
  line-height: 2;
}
</style>

