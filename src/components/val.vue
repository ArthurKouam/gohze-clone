<script setup>

  defineProps({
    img: String,
    title: String,
    content: String,
  })

</script>

<template>
  <div class=" flex flex-col gap-2">
    <div>
      <img class=" h-[100px] mx-auto" :src="img" alt="">
    </div>
    <div class=" flex flex-col gap-2 text-[#212529]">
      <p class=" text-center h-12 text-[15px] font-black">{{ title }}</p>
      <p class=" text-justify text-[12px]">{{ content }}</p>
    </div>
  </div>
</template>