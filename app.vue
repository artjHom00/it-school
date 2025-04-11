<script setup lang="ts">
</script>

<template>
  <div class="h-screen relative overflow-x-hidden bg-white dark:bg-zinc-900 transition-colors duration-100 text-gray-800 dark:text-white">
    <div class="absolute bottom-96 -left-3/7 w-3/5 h-[70vh] bg-blue-500/80 rounded-full blur-[999px] opacity-30 overflow-hidden"></div>
    <div class="absolute top-0 -right-1/2 w-1/2 h-[70vh] bg-blue-500/60 rounded-full blur-[999px] opacity-30 overflow-hidden"></div>

    <Header class="z-50 relative" />
    <main class="relative container mx-auto px-4 py-8 md:py-24 flex flex-col md:flex-row items-center z-50">
      <div class="w-full md:w-1/2 text-center md:text-left mb-8 md:mb-0">
        <h1 class="text-4xl sm:text-6xl font-bold mb-8 text-center">
          Запишитесь на пробное занятие в 
          <span class="inline-block decoration-primary relative">
            <span class="relative z-10">IT-Школе</span>
            <span class="bottom-0 absolute bg-orange-200 dark:bg-range-600 opacity-50 h-4 md:h-6 md:-bottom-0.5 -inset-x-0.5 sm:-inset-x-2"></span>
          </span>
        </h1>
        <div class="flex flex-col items-center md:items-start">
          <UiButton variant="primary" class="mx-auto w-2/3 text-white font-bold py-3 px-8 rounded-lg text-lg mb-4 transition-colors">
            Начать
          </UiButton>
          <NuxtLink to="#" class="mx-auto w-fit text-blue-500 focus:underline hover:underline">
            У меня уже есть аккаунт
          </NuxtLink>
        </div>
      </div>

      <div class="w-full md:w-1/2 flex justify-center">
        <div class="robot-container w-64 h-64 md:w-96 md:h-96 relative">
          <img src="/images/it.png" class="absolute mx-auto"/>
          <img src="/images/robot.svg" class="w-2/3 animate-bounce mx-auto"/>
        </div>
      </div>

    </main>
  </div>
</template>

<style>
@keyframes bounce {
  0%, 100% {
    transform: scale(0.99) translateY(-3%);
    animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
  }
  50% {
    transform: scale(1) translateY(0);
    animation-timing-function: cubic-bezier(0, 0, 0.2, 1);
  }
}

.animate-bounce {
  animation: bounce 1.5s infinite;
}

</style>