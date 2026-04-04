<script lang="ts" setup>
import type { MenuProps } from 'ant-design-vue';

const props = withDefaults(defineProps<MenuProps>(), {
  mode: 'horizontal',
});
</script>

<template>
  <a-menu :mode="props.mode" :items="props.items" />
</template>
