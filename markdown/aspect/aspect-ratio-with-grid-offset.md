# 在偏移的网格上对齐

使用`lock-aspect-ratio`时，在网格上使用组件的成本并不是很好。 您可以通过拖动（例如右手柄或底部手柄）来注意到您有不同的结果。


```html
<template>
  <div class="view-box">
    <div id="toolbar"></div>
    <div class="container">
      <div :style="style">
        <VueDragResizeRotate :grid="[20, 40]" :x="10" :y="20" :minh="30" :minw="30" :lock-aspect-ratio="true">
          <p>Aspect ratio in Grid 20x40 starting with a 10x20 offset</p>
        </VueDragResizeRotate>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      style: {
        position: "relative",
        backgroundColor: "#808080",
        height: "100%",
        background:
          "linear-gradient(-90deg, rgba(0, 0, 0, .1) 1px, transparent 1px), linear-gradient(rgba(0, 0, 0, .1) 1px, transparent 1px)",
        backgroundSize: "20px 40px, 20px 40px",
        backgroundPosition: "10px 20px"
      }
    };
  }
};
</script>
```
