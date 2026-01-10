<template>
  <div class="slidev-layout two-col-60-40 h-full grid grid-cols-[1fr_1fr] gap-4 p-8">
    <div class="flex flex-col justify-center overflow-hidden">
      <slot />
    </div>
    <div class="flex items-center justify-center overflow-hidden">
      <img v-if="$props.image" :src="$props.image" class="max-w-full max-h-full object-contain" />
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: String
})
</script>