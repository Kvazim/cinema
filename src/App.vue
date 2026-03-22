<script setup lang="ts">
import TokenProvider from './shared/hock/TokenProvider.vue';
import { TEME_CONFIG } from './shared/lib/theme';
import UiHeader from './shared/ui/Uiheader/UiHeader.vue';
</script>

<template>
  <TokenProvider :theme-config="TEME_CONFIG">
    <a-layout class="layout">
      <UiHeader />
    </a-layout>
  </TokenProvider>
</template>

<style scoped>
.layout {
  min-height: 100vh;
}
</style>
