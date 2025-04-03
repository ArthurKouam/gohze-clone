<script setup>
  defineProps({
    img: String,
    text: String
  })
</script>

<template>
  <div class=" w-full rounded-3xl bg-gray-200 text-[#4B2F00] p-4">
    <img class=" h-[60px] mx-auto" :src="img" alt="">
    <p class=" my-4 text-center font-medium">{{ text }}</p>
  </div>
</template>