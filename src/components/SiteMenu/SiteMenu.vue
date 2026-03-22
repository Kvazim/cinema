<script lang="ts" setup>
import UiLogo from '@/shared/ui/UiLogo.vue/UiLogo.vue';
import type { MenuProps } from 'ant-design-vue';

import { h, ref } from 'vue';
import { RouterLink } from 'vue-router';

const current = ref<string[]>(['mail']);
const items = ref<MenuProps['items']>([
  {
    key: 'mail',
    label: 'Navigation One',
    title: 'Navigation One',
  },
  {
    key: 'app',
    label: 'Navigation Two',
    title: 'Navigation Two',
  },
  {
    key: 'alipay',
    label: h(RouterLink, { to: '/films' }, 'Films'),
    title: 'Films',
  },
]);
</script>

<template>
  <a-layout-header>
    <UiLogo />
    <a-menu v-model:selectedKeys="current" mode="horizontal" :items="items" />
  </a-layout-header>
</template>
