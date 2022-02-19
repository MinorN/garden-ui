<template>
  <div>
    <h1>Button 示例</h1>
    <section class="first-section">
      <h2><span>#</span>常规使用</h2>
      <p>使用<span>theme</span>属性来改变<span>Button</span>组件的样式</p>
      <Demo :component="ButtonTheme"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持size</h2>
      <p>使用<span>size</span>属性来改变<span>Button</span>组件的大小</p>
      <Demo :component="ButtonSize"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持loading</h2>
      <p>使用<span>loading</span>属性来改变<span>Button</span>组件的加载状态</p>
      <Demo :component="ButtonLoading"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持level</h2>
      <p>使用<span>level</span>属性来改变<span>Button</span>组件的重要等级</p>
      <Demo :component="ButtonLevel"/>
    </section>
    <section class="first-section">
      <h2><span>#</span>支持disabled</h2>
      <p>使用<span>disabled</span>属性来改变<span>Button</span>组件的状态</p>
      <Demo :component="ButtonDisabled"/>
    </section>
  </div>
  <div class="next">
    <router-link to="/doc/switch">上一节：Switch组件</router-link>
    <router-link to="/doc/dialog">下一节：Dialog组件</router-link>
  </div>
</template>


<script lang="ts">
import Demo from './Demo.vue';
import Button from '../lib/Button.vue';
import ButtonSize from './ButtonComponents/ButtonSize.vue';
import ButtonLoading from './ButtonComponents/ButtonLoading.vue';
import ButtonTheme from './ButtonComponents/ButtonTheme.vue';
import ButtonLevel from './ButtonComponents/ButtonLevel.vue';
import ButtonDisabled from './ButtonComponents/ButtonDisabled.vue';

export default {
  components: {Demo, Button},
  setup() {
    return {ButtonSize, ButtonLoading, ButtonTheme, ButtonLevel, ButtonDisabled};
  }
};
</script>

<style lang="scss" scoped>
span {
  color: red;
  line-height: 2;
}
.next{
  display: flex;
  justify-content: space-between;
}
</style>
