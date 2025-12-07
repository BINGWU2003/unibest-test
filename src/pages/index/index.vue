<script lang="ts" setup>
import { safeAreaInsets } from '@/utils/systemInfo'

defineOptions({
  name: 'Home',
})
definePage({
  // 使用 type: "home" 属性设置首页，其他页面不需要设置，默认为page
  type: 'home',
  style: {
    // 'custom' 表示开启自定义导航栏，默认 'default'
    navigationStyle: 'custom',
    navigationBarTitleText: '首页',
  },
})

console.log('index/index 首页打印了')

onLoad(() => {
  console.log('测试 uni API 自动引入: onLoad')
})
</script>

<template>
  <view class="bg-white px-4 pt-2" :style="{ marginTop: `${safeAreaInsets?.top}px` }">
    <view class="mt-10">
      <image src="/static/logo.svg" alt="" class="mx-auto block h-28 w-28" />
    </view>
    <view class="mt-4 text-center text-4xl text-[#d14328]">
      unibest best
    </view>
    <view class="mb-8 mt-2 text-center text-2xl">
      最好用的 uniapp 开发模板
    </view>
  </view>
</template>
