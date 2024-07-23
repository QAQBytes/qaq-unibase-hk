<route lang="json5" type="home">
{
  layout: 'layout-uvui',
  style: {
    navigationBarTitleText: '首页',
  },
}
</route>

<template>
  <view class="page">
    <layout-uvui />
  </view>
</template>

<script lang="ts" setup>
defineOptions({
  name: 'Home',
})
</script>

<style>
.page {
  padding: 20px;
}
</style>
