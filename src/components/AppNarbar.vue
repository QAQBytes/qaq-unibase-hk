<template>
  <view>
    <uv-navbar leftText="返回" :fixed="false" title="个人中心" :safeAreaInsetTop="false">
      <template v-slot:left>
        <view class="uv-nav-slot">
          <uv-icon name="arrow-left" size="19"></uv-icon>
          <uv-line direction="column" :hairline="false" length="16" margin="0 8px"></uv-line>
          <uv-icon name="home" size="20"></uv-icon>
        </view>
      </template>
    </uv-navbar>
  </view>
</template>
<style scoped lang="scss">
@mixin flex($direction: row) {
  /* #ifndef APP-NVUE */
  display: flex;
  /* #endif */
  flex-direction: $direction;
}
.uv-nav-slot {
  @include flex;
  align-items: center;
  justify-content: space-between;
  padding: 3px 7px;
  border-color: #dadbde;
  border-width: 0.5px;
  border-radius: 100px;
  opacity: 0.8;
}
</style>
