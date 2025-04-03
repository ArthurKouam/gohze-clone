<script setup>
</script>

<template>
  <footer class=" bg-black text-white">
    <div class="max-w-[1200px] px-4 py-[65px] mx-auto flex gap-10 lg:gap-16 flex-col justify-center md:flex-row">
      <div class=" flex flex-col md:flex-1/3 gap-3">
        <img src="@/assets/logo.png" class=" w-[200px]" alt="">
        <p class=" font-bold">Let´s move to the next step</p>
        <p></p>
      </div>

      <div class=" flex flex-col md:flex-1/3">
        <div class="uppercase font-black text-[20px] mb-1.5">Nos services d' Expertise</div>
        <ul class="yellow flex flex-col gap-3 font-light text-[15px]">
          <li>Conception de sites WEB</li>
          <li>Conception d'Applications</li>
          <li>Dématérialisation des procédures</li>
          <li>Dimensionnement des réseaux</li>
          <li>Gestion de bases de données</li>
          <li>Graphic design</li>
          <li>Marketing digital</li>
        </ul>
      </div>

      <div class="md:flex-1/3">
        <div class="uppercase font-black text-[20px] mb-1.5">
          Contacts
        </div>
        <div class="flex flex-col gap-1 font-bold">
          <p>Téléphone</p>
          <p class="text-[#ffb500]">+237 697090659/697257887/671826822</p>
          <p>Adresse Mail</p>
          <p class="text-[#ffb500]">contact@gohze.org</p>
          <p>Adresse</p>
          <p class="text-[#ffb500] font-light text-lg">Carrefour Biyem-ASSI, Face Général Voyages, Yaoundé, Cameroun</p>
          <p>Heures d’ouverture</p>
          <p class="text-[#ffb500] text-lg">Du lundi au vendredi : 8h00–18h00</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
  .yellow li{
    display: flex;
    gap: 5px;
    align-items: center;
  }

  .yellow li::before{
    content: "";
    display: block;
    height: 10px;
    width: 10px;
    background: #ffb500;
  }
</style>