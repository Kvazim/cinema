<script lang="ts" setup>
import SiteMenu from '@/components/SiteMenu/SiteMenu.vue';
import UiLogo from '@/shared/ui/UiLogo.vue/UiLogo.vue';

import type { MenuProps } from 'ant-design-vue';

import { h, ref } from 'vue';
import { RouterLink } from 'vue-router';

// const current = ref<string[]>(['/films']);
const items = ref<MenuProps['items']>([
  {
    key: 'films',
    label: h(RouterLink, { to: '/films' }, 'Фильмы'),
    title: 'Фильмы',
  },
  {
    key: 'serials',
    label: h(RouterLink, { to: '/serials' }, 'Сериалы'),
    title: 'Сериалы',
  },
  {
    key: 'playlists',
    label: h(RouterLink, { to: '/playlists' }, 'Подборки'),
    title: 'Подборки',
  },
]);
</script>

<template>
  <a-layout-header class="header">
    <UiLogo />
    <SiteMenu class="header__menu" :items="items" />
  </a-layout-header>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
}
.header__menu {
  opacity: 0.5;
}
</style>
