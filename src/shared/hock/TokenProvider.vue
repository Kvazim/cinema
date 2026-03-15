<script setup lang="ts">
import type { ThemeConfig } from 'ant-design-vue/es/config-provider/context'
defineProps<{
  themeConfig: ThemeConfig
}>()

</script>

<template>
  <a-config-provider :theme="themeConfig">
    <slot></slot>
  </a-config-provider>
</template>
