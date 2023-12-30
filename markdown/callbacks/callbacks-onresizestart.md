# onResizeStart回调的基本组件

具有`onResizeStart `回调的基本组件，带有<b>`onResizeStart` </b> prop，它接受在拖动开始时调用的函数（单击或触摸元素）。 如果函数返回`false`，则取消操作。 您可以使用此功能来防止事件冒泡。


```html
<template>
  <div class="view-box">
    <div id="toolbar">
      <p :style="style">
        I turn red when
        <i>onResizeStart</i>
        is called. Callback then prevents resizing.
      </p>
    </div>
    <div class="container">
      <VueDragResizeRotate :on-resize-start="onResizeStart"></VueDragResizeRotate>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      style: {
        color: "black"
      }
    };
  },
  methods: {
    onResizeStart(e) {
      console.log(e)
      this.style.color = "red";
      return false;
    }
  }
};
</script>
```
