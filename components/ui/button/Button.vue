<script lang="ts" setup>
defineProps({
  variant: {
    type: String,
    default: 'ghost',
    validator: (value: string) => ['primary', 'outline', 'ghost'].includes(value)
  },
  size: {
    type: String,
    default: 'md',
    validator: (value: string) => ['sm', 'md', 'lg'].includes(value)
  },
  disabled: {
    type: Boolean,
    default: false
  },
  type: {
    type: String as () => 'button' | 'submit' | 'reset',
    default: 'button',
    validator: (value: string) => ['button', 'submit', 'reset'].includes(value)
  }
})
</script>

<template>
  <button
    :type="type"
    :disabled="disabled"
    :class="[
      'inline-flex items-center justify-center rounded-lg font-medium cursor-pointer focus:outline-none focus:ring-0',
      {
        'bg-blue-500 transition-shadow hover:shadow-[7px_7px_0px_0px_rgba(249,_115,_22,_0.8)] hover:bg-blue-600': variant === 'primary',
        'bg-transparent border-2 border-blue-500 text-blue-500 hover:opacity-70': variant === 'outline',
        'p-3 transition-all relative top-0 hover:top-[-1px]': variant === 'ghost',
        'opacity-50 cursor-not-allowed': disabled
      }
    ]"
  >
    <slot />
  </button>
</template>