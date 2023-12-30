# 网格20x20像素

一个基本组件，用<b>`grid = [20,20]`</b> prop来设置网格单元的尺寸（高度和宽度，以像素为单位）。


```html
<template>
  <div class="view-box">
    <div id="toolbar">Size: {{ width }} x {{ height }}</div>
    <div class="container">
      <div :style="style">
        <VueDragResizeRotate :grid="[20, 20]" :x="0" :y="0" @resizing="onResizing">
          <p>Grid 20x20 starting from the top-left corner</p>
        </VueDragResizeRotate>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      width: 200,
      height: 200,
      style: {
        position: "relative",
        height: "100%",
        width: "100%",
        backgroundColor: "#808080",
        background:
          "linear-gradient(-90deg, rgba(0, 0, 0, .1) 1px, transparent 1px), linear-gradient(rgba(0, 0, 0, .1) 1px, transparent 1px)",
        backgroundSize: "20px 20px, 20px 20px"
      }
    };
  },
  methods: {
    onResizing(x, y, width, height) {
      this.width = width;
      this.height = height;
    }
  }
};
</script>
```
