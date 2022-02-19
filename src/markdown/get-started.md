# 开始使用
请先[安装](#/doc/install)本组件库.

然后在你的代码中写入下面的代码
```angular2html
import { Button, Tabs, Switch, Dialog } from "garden-ui"
```

就可以使用我提供的组件了。

## Vue单文件组件

代码示例：

```angular2html
<template>
  <div>
    <Button>按钮</Button>
  </div>
</template>
<script>
import {Button, Tabs, Switch, Dialog} from "garden-ui"
export default {
  components: {Button}
}
</script>
```
下一节：[Switch组件](#/doc/switch)