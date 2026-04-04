<script lang="ts" setup>
import TokenProvider from '@/shared/hock/TokenProvider.vue';
const { type, danger = false } = defineProps<{
  type?: 'primary' | 'ghost' | 'dashed' | 'link' | 'text' | 'default';
  danger?: boolean;
  href?: string;
}>();
</script>

<template>
  <TokenProvider
    :themeConfig="{
      components: {
        Button: {
          paddingContentHorizontal: 23,
          controlHeight: 55,
          borderRadius: 10,
          boxShadow: 'none',
          boxShadowSecondary: 'none',
          // danger
          colorErrorBg: '#ED0A32',
          colorErrorHover: '#ED0A32A3',
          // default button
          colorPrimaryHover: '#ffffffa1',
          colorPrimaryActive: '#ffffffa1',
          colorBgContainer: 'transparent',
          fontSize: 16,
          colorText: '#FFFFFF',
        },
      },
    }"
  >
    <a-button :to="href" class="ui-button" :type="type ?? 'default'" :danger="danger">
      <slot></slot>
    </a-button>
  </TokenProvider>
</template>

<style scoped>
.ui-button {
  font-weight: 600;
}
</style>
