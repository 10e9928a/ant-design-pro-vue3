<script setup lang="ts">
import type { CSSProperties } from 'vue'

const headerStyle = computed<CSSProperties>(() => {
  return {
    height: '48px',
    lineHeight: '48px',
    paddingInline: 0,
    zIndex: 19,
  }
})
</script>

<template>
  <a-layout-header :style="headerStyle" class="ant-pro-fixed-header-action">
    <div class="ant-pro-global-header">
      <div class="flex-1">
        <slot name="headerContent" />
      </div>
      <a-space flex-shrink-0>
        <slot name="headerActions" />
      </a-space>
    </div>
  </a-layout-header>
</template>

<style lang="less">
@import "./index.less";
</style>
