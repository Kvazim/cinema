<script lang="ts" setup>
import SiteMenu from '@/components/SiteMenu/SiteMenu.vue';
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
    <SiteMenu />
    <a-menu v-model:selectedKeys="current" mode="horizontal" :items="items" />
  </a-layout-header>
</template>
