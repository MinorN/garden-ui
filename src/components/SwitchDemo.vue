<template>
  <div>
    <h1>Switch 组件示例</h1>
    <section class="first-section">
      <h2><span>#</span>基础用法</h2>
      <p>使用<span>v-model</span>来绑定一个<span>Boolean</span>类型的变量到<span>Switch</span>组件</p>
      <Demo :component="SwitchNormal"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持disabled属性</h2>
      <p>在<span>Switch</span>组件中添加<span>disabled</span>属性，达到了<span>禁用Switch</span>组件的目的</p>
      <Demo :component="SwitchDisabled"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持loading属性</h2>
      <p>在<span>Switch</span>组件中添加<span>loading</span>属性，达到了<span>Switch</span>组件显示加载状态</p>
      <Demo :component="SwitchLoading"/>
    </section>
  </div>
</template>

<script lang="ts">
import SwitchNormal from './SwitchComponents/SwitchNormal.vue';
import SwitchDisabled from './SwitchComponents/SwitchDisabled.vue';
import SwitchLoading from './SwitchComponents/SwitchLoading.vue';
import Demo from './Demo.vue';

export default {
  components: {Demo},
  setup() {
    return {SwitchNormal, SwitchDisabled,SwitchLoading};
  }
};
</script>


<style lang="scss" scoped>
$border-color: #d9d9d9;
span{
  color: red;
  line-height: 2;
}
.demo {
  border: 1px solid $border-color;
  margin: 16px 0 32px;

  > h2 {
    font-size: 20px;
    padding: 8px 16px;
    border-bottom: 1px solid $border-color;
  }

  &-component {
    padding: 16px;
  }

  &-actions {
    padding: 8px 16px;
    border-top: 1px dashed $border-color;
  }

  &-code {
    padding: 8px 16px;
    border-top: 1px dashed $border-color;

    > pre {
      line-height: 1.1;
      font-family: Consolas, 'Courier New', Courier, monospace;
      margin: 0;
    }
  }
}
</style>

