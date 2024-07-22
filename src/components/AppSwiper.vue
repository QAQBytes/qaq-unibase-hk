<template>
  <uv-swiper
    :list="list"
    keyName="image"
    showTitle
    :title-style="{ color: 'red', textAlign: 'center' }"
    :autoplay="false"
    circular
  ></uv-swiper>
</template>

<script>
export default {
  name: 'AppSwiper',
  props: {
    list: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
}
</script>

<style scoped>
/* 你可以在这里添加组件的样式 */
</style>
