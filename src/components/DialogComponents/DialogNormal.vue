<demo>
基础用法
</demo>


<template>
  <div>
    <Button @click="toggle" level="main">打开Dialog</Button>
    <Dialog v-model:visible="showDialog" :closeOnClickOverly="false"></Dialog>
  </div>
</template>

<script lang="ts">
import Button from '../../lib/Button.vue';
import Dialog from '../../lib/Dialog.vue';
import {ref} from 'vue';

export default {
  components: {Dialog, Button},
  setup() {
    const showDialog = ref<Boolean>(false);
    const toggle = () => {
      showDialog.value = !showDialog.value;
    };
    return {showDialog, toggle};
  }
};
</script>