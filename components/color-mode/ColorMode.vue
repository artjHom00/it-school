<script setup lang="ts">
import { Icon } from '@iconify/vue'

const colorMode = useColorMode()

const handleThemeChange = () => {
  switch (colorMode.preference) {
    case 'light':
      colorMode.preference = 'dark'
      break;
    case 'dark':
      colorMode.preference = 'light'
      break;
    default:
      colorMode.preference = 'light'
      break;
  }
}
</script>

<template>
  <UiButton variant="ghost" @click="handleThemeChange">
    <Icon icon="radix-icons:moon"
      class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"/>
    <Icon icon="radix-icons:sun"
      class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"/>
    <span class="sr-only">Toggle theme</span>
  </UiButton>
</template>