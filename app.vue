<script setup lang="ts">
</script>

<template>
  <div class="h-screen relative bg-white dark:bg-zinc-900 transition-colors duration-100 text-gray-800 dark:text-white">
    <div class="absolute bottom-96 -left-3/7 w-3/5 h-[70vh] bg-blue-500/80 rounded-full blur-[999px] opacity-30 overflow-hidden"></div>
    <div class="absolute top-0 -right-1/2 w-1/2 h-[70vh] bg-blue-500/60 rounded-full blur-[999px] opacity-30 overflow-hidden"></div>

    <Header />

    <main class="container mx-auto px-4 py-8 md:py-16 flex flex-col md:flex-row items-center z-10">
      <div class="w-full md:w-1/2 text-center md:text-left mb-8 md:mb-0">
        <h1 class="text-2xl sm:text-6xl font-bold mb-8 text-center">
          Запишитесь на пробное занятие в IT-Школе
        </h1>
        <div class="flex flex-col items-center md:items-start">
          <UiButton variant="primary" class="mx-auto w-2/3 text-white font-bold py-3 px-8 rounded-lg text-lg mb-4 transition-colors">
            Начать
          </UiButton>
          <NuxtLink to="#" class="mx-auto w-fit text-blue-500 hover:underline">
            У меня уже есть аккаунт
          </NuxtLink>
        </div>
      </div>

      <div class="w-full md:w-1/2 flex justify-center">
        <div class="robot-container w-64 h-64 md:w-80 md:h-80 lg:w-96 lg:h-96 relative">
          <img src="/images/robot.svg" alt="IT School Robot" class="w-full h-full robot" />
        </div>
      </div>

    </main>
  </div>
</template>