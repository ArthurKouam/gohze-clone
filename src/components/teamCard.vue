<script setup>

  defineProps(['img', 'name', 'rule'])

</script>

<template>

  <div class=" flex flex-col gap-2.5 bg-white rounded-3xl shadow-xl p-1.5">
    <div>
      <img class=" mx-auto h-[140px]" :src="img" alt="">
    </div>
    <div class=" text-center font-bold mb-2 text-[12px]">
      <p class="text-[#4B2F00]">{{ name }},</p>
      <p class="uppercase text-[#FFB500]">{{ rule }}</p>
    </div>
  </div>

</template>