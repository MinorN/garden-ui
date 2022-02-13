<template>
  <div>
    <h2>Switch 组件示例</h2>
    <div>
      <h3><span>#</span> 基础用法 </h3>
      <p>使用<span>v-model</span>绑定一个<span>Boolean</span>类型的变量到<span>Switch</span>组件</p>
      <div class="demo">
        <h2>常规用法</h2>
        <div class="demo-component"><Switch v-model:value="bool"/></div>
        <div class="code-watch"><button>查看代码</button></div>
        <div class="code-demo">
          <pre class="code">
            <span class="tag"></span>
          </pre>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Switch from '../lib/Switch.vue';
import {ref} from 'vue';


export default {
  components: {Switch},
  setup() {
    const bool = ref(false);
    return {bool};
    }
};
</script>


<style lang="scss" scoped>
*{box-sizing: border-box;margin: 0;padding: 0}
span{
  color: red;
}

.demo{
  max-width: 500px;
  display: block;
  flex-wrap: wrap;
  border:1px solid #333;
  border-radius: 5px;
  margin: 16px 32px;
  >h2{
    font-size: 20px;
    padding: 8px 16px;
    height: 40px;
    width: 100%;
    border-bottom: 1px solid #333;
  }
  >.demo-component{
    padding: 20px 16px;
  }
  >.code-watch{
    padding: 8px 16px;
    border-top: 1px solid #333;
    >button{
      height: 32px;
      padding: 0 12px;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #fff;
      color: #333;
      border-radius: 5px;
      white-space: nowrap;
      margin: 0 10px 8px 0;
      border:1px solid #333;
    }
  }
}
</style>

