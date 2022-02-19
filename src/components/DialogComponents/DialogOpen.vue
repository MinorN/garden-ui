<demo>
一键打开Dialog
</demo>


<template>
  <div>
    <Button level="main" @click="toggle">打开dialog</Button>
  </div>
</template>

<script lang="ts">
import Button from '../../lib/Button.vue';
import {openDialog} from '../../lib/openDialog.ts';
import {ref,h} from 'vue';
export default {
  components: {Button},
  setup() {
    const toggle = ()=>{
      openDialog({
        title:h('strong',{},'标题'),
        content:'这里是内容',
        ok(){
          console.log('ok')
        },
        cancel(){
          console.log('cancel')
        }
      })
    }
    return {toggle}
  }
};
</script>
