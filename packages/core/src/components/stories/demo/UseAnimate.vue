<script setup lang="ts">
import { onMounted } from 'vue'
import { useAnimate } from '../../../index.ts'

const { animate, scope } = useAnimate()

onMounted(() => {
  animate(
    'li',
    {
      animate: {
        opacity: 0,
        x: 10,
      },
      transition(index) {
        return {
          opacity: {
            delay: index * 0.5,
          },
          x: {
            delay: index * 0.5,
          },
        }
      },
    },
  )
})

</script>

<template>
  <ul :ref="scope.registerElement">
    @oku/motion useAnimate Demo
    <li class="bg-red-500">
      1
    </li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
  </ul>
</template>
