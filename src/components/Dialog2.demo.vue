<demo>一键打开 Dialog</demo>
<template>
  <div><Button @click="showDialog">打开对话框</Button></div>
</template>
<script lang="ts">
import Button from '../lib/Button.vue'
import { openDialog } from '../lib/openDialog'
import { h, ref } from 'vue'
export default {
  components: { Button },
  setup() {
    const showDialog = () => {
      openDialog({
        title: h('strong', {}, '标题'),
        content: '你好',
        closeOnClickOverlay: false,
        ok() {},
        cancel() {}
      })
    }
    return { showDialog }
  }
}
</script>>