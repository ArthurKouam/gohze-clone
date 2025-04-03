<script setup>
import { onMounted, ref } from 'vue'
import { RouterView } from 'vue-router'
import footerC from './components/footerC.vue';

onMounted(()=>{
  window.addEventListener('scroll', handle);
})

const scroll = ref(false)

const handle = ()=>{
  const pos = window.scrollY;
  console.log(pos)
  if(pos > 0) scroll.value = true
  else scroll.value = false
}
</script>

<template>
  <header :class="{ 'noir': scroll }" class=" w-full fixed top-0 left-0 z-50">
    <nav class="max-w-[1200px] px-4 py-3 mx-auto flex items-center justify-between">
      <div><img class=" h-12" src="@/assets/logo.png" alt=""></div>
      <ul class="hidden lg:flex items-center gap-3 text-white font-extrabold">
        <li>service</li>
        <li>Nos realisations</li>
        <li class=" bg-white text-black rounded px-6 py-1 font-light">Récevoir un dévis en 24h</li>
        <li><img class="h-4" src="@/assets/flag.svg" alt=""></li>
      </ul>
      <div class="lg:hidden text-white border border-white rounded p-2">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-align-justify-icon lucide-align-justify"><path d="M3 12h18"/><path d="M3 18h18"/><path d="M3 6h18"/></svg>
      </div>
    </nav>
  </header>

  <RouterView />

  <footerC></footerC>

</template>

<style scoped>
  .noir{
    background-color: rgba(0, 0, 0, 0.9);
  }
</style>
