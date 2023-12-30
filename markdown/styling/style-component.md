# 具有自定义类名的组件

具有自定义类名的组件，由prop <b>`class-name` </b>提供。

```html
<template>
  <div class="view-box">
    <div id="toolbar">具有自定义类名的组件</div>
    <div class="container">
      <VueDragResizeRotate class-name="my-class">
        <p>
          你可以给组件设置一个类名，覆盖其默认类名
          <b>class-name</b>
        </p>
      </VueDragResizeRotate>
    </div>
  </div>
</template>

<style scoped>
.my-class {
  border: 1px solid red;
  -webkit-transition: background-color 200ms linear;
  -ms-transition: background-color 200ms linear;
  transition: background-color 200ms linear;
}
</style>
```
