<script lang="ts" setup>
import IconLogo from '@/shared/icons/IconLogo.vue';
</script>

<template>
  <RouterLink class="logo" to="/">
    <IconLogo />
  </RouterLink>
</template>

<style scoped>
.logo {
  display: block;
  width: 170px;
  height: 32px;
}

.logo:hover {
  opacity: 0.8;
}
</style>
