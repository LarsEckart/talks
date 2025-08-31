<template>
  <div class="slidev-layout two-col-60-40 h-full grid grid-cols-[3fr_2fr] gap-6">
    <div class="pr-4">
      <slot />
    </div>
    <div class="flex items-center justify-center">
      <img v-if="$props.image" :src="$props.image" class="max-w-full max-h-full object-contain" />
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: String
})
</script>