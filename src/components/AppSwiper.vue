<template>
  <uv-swiper
    :list="list"
    keyName="image"
    showTitle
    :title-style="{ color: 'red', textAlign: 'center' }"
    :autoplay="true"
    :interval="3000"
    :duration="500"
    circular
    :height="200"
    indicator
    indicatorActiveColor="#FF0000"
    indicatorInactiveColor="#FFFFFF"
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

<style scoped></style>
