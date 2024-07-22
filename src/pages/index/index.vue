<route lang="json5" type="home">
{
  style: {
    navigationBarTitleText: '首页',
  },
}
</route>
<template>
  <view class="bg-white overflow-hidden pt-2 px-4">
    <!-- 轮播图 -->
    <view class="swiper-container">
      <AppSwiper :list="swiperList" />
    </view>
    <view class="mt-12">
      <image src="/static/logo.svg" alt="" class="w-28 h-28 block mx-auto" />
    </view>
    <view class="text-center text-4xl main-title-color mt-4">unibest</view>
    <view class="text-center text-2xl mt-2 mb-8">最好用的 uniapp 开发模板</view>

    <view class="text-justify max-w-100 m-auto text-4 indent mb-2">{{ description }}</view>
    <view class="text-center mt-8">
      当前平台是：
      <text class="text-green-500">{{ PLATFORM.platform }}</text>
    </view>
    <view class="text-center mt-4">
      模板分支是：
      <text class="text-green-500">base</text>
    </view>
    <view class="m-4 flex">
      <uv-icon name="home"></uv-icon>
      <uv-icon name="home" color="red"></uv-icon>
      <uv-icon name="home" class="text-green"></uv-icon>
    </view>
  </view>
</template>

<script lang="ts" setup>
import PLATFORM from '@/utils/platform'
import AppSwiper from '@/components/AppSwiper.vue'
import { ref, onMounted } from 'vue'

defineOptions({
  name: 'Home',
})

// 获取屏幕边界到安全区域距离
const safeAreaInsets = ref({ top: 0 })
onMounted(() => {
  const systemInfo = uni.getSystemInfoSync()
  safeAreaInsets.value.top = systemInfo.statusBarHeight + 44 // 假设导航栏高度为44px
})

const author = ref('菲鸽')
const description = ref(
  'unibest 是一个集成了多种工具和技术的 uniapp 开发模板，由 uniapp + Vue3 + Ts + Vite4 + UnoCss + UniUI + VSCode 构建，模板具有代码提示、自动格式化、统一配置、代码片段等功能，并内置了许多常用的基本组件和基本功能，让你编写 uniapp 拥有 best 体验。',
)

const swiperList = [
  {
    image: 'https://cdn.uviewui.com/uview/swiper/swiper2.png',
    title: '丙辰中秋，欢饮达旦，大醉，作此篇，兼怀子由',
  },
  {
    image: 'https://cdn.uviewui.com/uview/swiper/swiper1.png',
    title: '明月几时有？把酒问青天',
  },
  {
    image: 'https://cdn.uviewui.com/uview/swiper/swiper3.png',
    title: '不知天上宫阙，今夕是何年',
  },
]
</script>

<style>
/* 调整轮播图容器样式，确保位置正确 */
.swiper-container {
  position: fixed;
  top: var(--safe-area-top); /* 使用 CSS 变量 */
  right: 8px; /* 设置右边距 */
  left: 8px; /* 设置左边距 */
  z-index: 999;
  width: calc(100% - 16px); /* 给左右两边留出8px的空隙 */
  margin: 0 auto; /* 居中 */
}

.content {
  padding: 20px;
  margin-top: 200px; /* 确保内容区域不被轮播图遮挡，值应与轮播图高度相同 */
}

.main-title-color {
  color: #d14328;
}
</style>
