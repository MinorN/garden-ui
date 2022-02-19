<demo>
支持closeOnClickOverlay
</demo>

<template>
  <div>
    <Button level="danger" @click="toggle">打开dialog</Button>
    <Dialog v-model:visible="showDialog" :closeOnClickOverlay="false">
      <p>不能点击遮罩层关闭</p>
    </Dialog>
  </div>
</template>

<script lang="ts">
import Button from '../../lib/Button.vue';
import Dialog from '../../lib/Dialog.vue';
import {ref} from 'vue';

export default {
  components: {Dialog, Button},
  setup() {
    const showDialog = ref(false);
    const toggle = () => {
      showDialog.value = !showDialog.value;
    };
    return {showDialog, toggle};
  }
};
</script>