<script setup lang="ts">
import { Motion } from '@oku-ui/motion'
</script>

<template>
  <Motion
    class="bg-white size-52 aspect-square rounded-2xl"
    :initial="{ scale: 0 }"
    :animate="{ rotate: 180, scale: 1 }"
    :transition="{
      type: 'spring',
      stiffness: 260,
      damping: 20,
      delay: 0.3,
    }"
  />
</template>
