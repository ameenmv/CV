<template>
  <div class="min-h-screen flex items-center justify-center bg-[#1e4137] overflow-hidden">
    <div ref="box" class="p-12 bg-[#FFF7F0] rounded-[30px] shadow-2xl flex flex-col items-center gap-6">
      <h1 class="text-4xl md:text-6xl font-bold text-[#0b1311]">
        Welcome to Your New Portfolio!
      </h1>
      <p class="text-lg text-gray-700">
        Nuxt 3 + Tailwind CSS + GSAP are perfectly installed.
      </p>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
const { $gsap } = useNuxtApp()

const box = ref(null)

onMounted(() => {
  $gsap.from(box.value, {
    y: 100,
    opacity: 0,
    duration: 1.2,
    ease: 'power3.out'
  })
})
</script>
