<script setup lang="ts">
import { Motion } from '@oku-ui/motion'
</script>

<template>
  <Motion
    class="bg-white size-52 aspect-square rounded-2xl"
    :initial="{ scale: 0 }"
    :in-view="{ rotate: 180, scale: 1 }"
    :in-view-options="{
      once: true,
    }"
    :transition="{
      type: 'spring',
      stiffness: 260,
      damping: 20,
      delay: 0.3,
    }"
  />
</template>
