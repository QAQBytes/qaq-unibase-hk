<template>
  <view class="layout-uvui">
    <slot />
    <uv-row />
    <uv-col />
  </view>
</template>
<style lang="scss">
.demo-layout {
  height: 25px;
  border-radius: 4px;
}
.bg-purple {
  background: #ced7e1;
}
.bg-purple-light {
  background: #e5e9f2;
}
.bg-purple-dark {
  background: #99a9bf;
}
</style>
