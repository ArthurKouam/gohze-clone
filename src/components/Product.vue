<script setup>

  const props = defineProps({
    open: {
      type: Boolean,
    },
    index: {
      type: Number,
    }
  })

  const emit = defineEmits(['update'])

  const toggle = () => {
    emit('update', props.index)
  }
</script>

<template>
  <div class=" border-b-2 pb-[10px] border-[hsla(0,0%,43.9%,.25)]">
      <div class=" flex justify-between items-center pb-[10px]">
        <div class=" flex items-center gap-1">
          <img class=" h-[50px]" src="@/assets/dsf.webp" alt="">
          <span class=" text-[#545454] text-lg uppercase font-black">Bonjour</span>
        </div>
        <button @click="toggle" class=" rounded-full cursor-pointer bg-gray-100 p-2">
          <svg :class="{ 'rotate-180': open }"
            class="w-4 h-4 transition-transform duration-300"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
          </svg>
        </button>
      </div>
      <div :class=" { 'max-h-0': !open, 'max-h-[800px]': open }" class="transition-all duration-500 flex flex-col md:flex-row items-center justify-center overflow-hidden">
        <div class=" md:flex-1/3">
          <p class=" font-light text-[#212529]">
            UPGESCO est un ERP développé par GOHZE permettant la gestion optimisée et complète de 06 aspects de l’activité d’une entreprise : <br>
            - Le CRM (gestion de relation client) <br>
            - La gestion de projets (Planification, suivi et évaluation) <br>
            - La gestion financière (Comptabilité, achats, ventes) <br>
            - La gestion logistique (Approvisionnement, gestion entrepôts, livraisons) <br>
            - La gestion de ressources humaines (Contrats, paie, Recrutement) <br>
            - La gestion de la production (digitalisation du processus de transformation de matières premières en produits finis)
          </p>
        </div>
        <div class=" md:flex-2/3">
          <img class="w-full" src="/src/assets/erp.webp" alt="">
        </div>
      </div>
    </div>
</template>