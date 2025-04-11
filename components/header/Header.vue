<script setup lang="ts">
import { Icon } from '@iconify/vue'

</script>

<template>
    <header class="container mx-auto px-4 py-6 flex justify-between items-center">
      <NuxtLink to="/" class="flex gap-3 items-center">
        <img src="/images/logo.svg" width="36" alt="">
        <span class="font-bold">IT-Школа</span>
      </NuxtLink>
      <div class="flex gap-4">
        <UiButton class="cursor-pointer">
          <Icon icon="streamline:programming-web-server-world-internet-earth-www-globe-worldwide-web-network" class="h-[1.2rem] w-[1.2rem]" />
        </UiButton>
        <ColorMode/>
      </div>
    </header>
</template>