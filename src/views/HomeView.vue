<script setup>
  import { ref } from 'vue';

  import expCard from '@/components/expCard.vue';
  import Product from '@/components/Product.vue';
  import val from '@/components/val.vue';
  import teamCard from '@/components/teamCard.vue';
  import 'vue3-carousel/carousel.css'
  import { Carousel, Slide, Navigation } from 'vue3-carousel'

  const open = ref(1)

  const change = (index)=>{
    console.log(index)
    if(open.value == index) open.value = 0;
    else open.value = index
  }

  const config = {
    itemsToShow: 4,
    gap: 5,
  }

  const vals = [
    {
      img: "/i1.svg",
      title: "Création de la valeur client",
      content: "Nous mesurons notre succès grâce à notre impact sur l’activité de nos clients. Nous tenons nos promesses, ce qui nous permet d'établir des relations à long terme",
    },
    {
      img: "/i2.svg",
      title: "Travailler pour toujours être le premier",
      content: "Nous faisons confiance à la créativité de chaque collaborateur ce qui nous permet d’augmenter notre capacité d’innovation et d’être ainsi plus près de nos clients",
    },
    {
      img: "/i4.svg",
      title: "Soyez audacieux et différent",
      content: "Nous agissons de façon différente afin de bousculer les situations établies à l’avance en essayant de nouvelles idées et de nouvelles approches.",
    },
    {
      img: "/i5.svg",
      title: "Apprendre et avancer ensemble",
      content: "Nous valorisons la diversité des points de vue, des idées et des profils ainsi qu’un partage de connaissances entre les collaborateurs ce qui favorise l’éclosion des talents.",
    },
  ]

  const teams = [
    {
      img: "/kennedy.webp",
      name: "Armel MANFOUO",
      rule: "Directeur Général"
    },
    {
      img: "/boris.webp",
      name: "Boris FOADING",
      rule: "Directeur technique"
    },
    {
      img: "/raoul.webp",
      name: "Raoul DZOUKOU",
      rule: "Directeur Financier et Chef de Projet"
    },
    {
      img: "/kevin.webp",
      name: "Kevin Teguia",
      rule: "Business Developer et Chef de Projet"
    },
    {
      img: "/joseph.webp",
      name: "Tentchou Joseph",
      rule: "Directeur Commercial"
    },
  ]
</script>

<template>
  <div class="">
    <div class="w-full h-[550px] md:h-[730px] flex items-center justify-center relative">
      <div class="absolute inset-0 bg-cover bg-center z-0" style="background-image: url('/hero.webp');"></div>
      <div class="max-w-[1200px] px-4 mx-auto text-center text-white z-10 pt-[50px]">
        <div class="mx-auto flex flex-col items-center justify-center max-w-[600px] gap-3">
          <h1 class=" uppercase font-black text-[23px] md:text-[27px]">Developpez votre entreprise avec le <br> meilleur des outils numériques</h1>
          <p class=" text-sm">
            GOHZE représente la crème de la crème dans l’univers des services numériques ! Rejoignez-nous et transformons ensemble votre entreprise grâce à nos offres de services. <br>
            <span class=" font-semibold">Join us to move your business to the next step</span>
          </p>
          <div class=" flex gap-7 w-full">
            <button class=" rounded w-full py-2 text-black bg-[#FFB500]">Bésoin d'un dévis?</button>
            <button class=" rounded w-full py-2 text-[#FFB500] border border-[#FFB500]">Découvrir nos offres personnalisées</button>
          </div>
        </div>
        
      </div>
    </div>

    <div class=" mt-[65px] w-full">
      <div class=" max-w-[1200px] px-4 mx-auto">
        <div class=" w-full">
          <h2 class="uppercase text-[#4B2F00] font-black text-[27px]">Améliorez votre <span class="text-[#FFB500]">business grâce</span> <br>
            à nos offres d’expertise !
          </h2>
          <p class=" text-[15px] my-4 text-[#9D9D9D]">
            Vous êtes une entreprise ou un porteur de projet ? Profitez de notre gamme de services de très haute qualité pour optimiser votre activité, vos opérations au quotidien, vous démarquer de vos concurrents par l’innovation et ainsi améliorer votre rentabilité
          </p>
          <div class=" mt-[30px] grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5   gap-5 flex-row">
            <expCard :img="'/web.webp'" :text="'Développement web, maintenance et hébergement'"></expCard>
            <expCard :img="'/mobile.webp'" :text="'Développement mobile Android et iOS, maintenance et hébergement'"></expCard>
            <expCard :img="'/desig.webp'" :text="'Branding, Design graphique, conception de visuels et supports de communication'"></expCard>
            <expCard :img="'/ui-ux.webp'" :text="'Design ou remodelage d’interfaces de sites web et d’applications web et mobile'"></expCard>
            <expCard :img="'/consulting.webp'" :text="'Conseil et accompagnement IT'"></expCard>
          </div>
        </div>
      </div>
    </div>

    <div class=" mt-[65px] w-full">

      <div class=" max-w-[1200px] px-4 mx-auto">
        <h2 class="uppercase text-[#4B2F00] font-black text-[27px] mb-4">
          DECOUVREZ NOS PRODUITS
        </h2>

        <div class=" flex flex-col gap-4">
          <Product  @update="change" v-for="n in 5" :open="n == open" :index="n"></Product>
        </div>
      </div>

    </div>

    <div class=" mt-[65px] w-full bg-gray-100 py-10">
      <div class=" max-w-[1200px] px-4 mx-auto">
        <h2 class="uppercase text-[#4B2F00] text-center font-black text-[27px] mb-4">
          let's move <span class="text-[#FFB500]">to the next step</span>
        </h2>

        <div class=" mt-9 grid grid-cols-1 gap-7 md:grid-cols-2 lg:grid-cols-4">
          <val v-for="vale in vals" :img="vale.img" :content=" vale.content" :title="vale.title"></val>
        </div>

      </div>
    </div>

    <div class=" mt-[65px] w-full ">
      <div class=" max-w-[1200px] px-4 mx-auto flex flex-col lg:flex-row items-center justify-center gap-9">
        
        <div class=" flex-1/2 text-[#4B2F00] text-justify">
          <h2 class="uppercase font-black text-[27px] mb-4">
            <span class="text-[#FFB500]">04 raisons</span> de travailler avec nous
          </h2>
          <p class=" text-[15px]">
            Nous pilotons vos projets de A à Z , Conscients qu'en raison de la taille, la complexité et les spécificités de certains projets, il n'est pas toujours évident pour les entreprises de les piloter tout en restant concentré sur son coeur de métier. C'est la raison pour laquelle nous proposons, tout en vous laissant l'exclusivité dans la prise des décisions, de vous accompagner dans ce secteur précis.
          </p>

          <p class="ext-[15px] mt-5">
            De facto, en amont, GOHZE vous assiste dans la description de votre besoin, l’étude d'impact et de faisabilité, la rédaction du cahier des charges. En aval, nos experts prodiguent des conseils et prennent en charge la conduite du projet afin de garantir le respect des exigences en termes de contenu, qualité, coût et délai.
          </p>

          <div class="font-black mt-9">
            <p>Besoin de solution informatique pour vos projets ? Contactez-nous</p>
            <p class=" text-2xl">+237 697090659 / 682536922</p>
          </div>
        </div>

        <div class="uppercase font-bold text-[15px] flex-1/2 grid grid-cols-1 gap-4 text-center md:grid-cols-2 ">
          <div class=" flex flex-col gap-3">
            <img class=" rounded-3xl shadow-xl" src="@/assets/quality.webp" alt="">
            <p>flexibilité et adaptabilité des services</p>
          </div>
          <div class=" flex flex-col gap-3">
            <img class=" rounded-3xl shadow-xl" src="@/assets/quality.webp" alt="">
            <p>Méthodologie adaptée au client</p>
          </div>
          <div class=" flex flex-col gap-3">
            <img class=" rounded-3xl shadow-xl" src="@/assets/quality.webp" alt="">
            <p>Qualité de la relation client</p>
          </div>
          <div class=" flex flex-col gap-3">
            <img class=" rounded-3xl shadow-xl" src="@/assets/quality.webp" alt="">
            <p>Gestion minutieuse de la production</p>
          </div>
        </div>

      </div>
    </div>

    <div class="relative mt-[65px] w-full py-14">
      <div class="z-0 absolute inset-0 bg-center bg-cover" style="background: url('/bg-stats.webp');"></div>
      <div class="z-10 relative max-w-[1200px] px-4 mx-auto">
        <div>
          <h2 class="uppercase text-[#4B2F00] text-center font-black text-[27px] mb-4">
            GOHZE EN QUELQUES CHIFFRES
          </h2>
          <p class=" text-xs text-center mt-1">
            Nous vous donnons rendez-vous au sommet ; ce n’est que le début ; nous passons à la prochaine <br> étape avec vous !
          </p>
        </div>

        <div class="font-black text-center mt-9 grid grid-cols-1 gap-5 gap-y-10 md:grid-cols-2 lg:grid-cols-4">
          <div>
            <p class=" text-6xl">+03</p>
            <p class="text-2xl mt-2">années d'experience</p>
          </div>
          <div>
            <p class=" text-6xl">+25</p>
            <p class="text-2xl mt-2">collaborateurs</p>
          </div>
          <div>
            <p class=" text-6xl">95%</p>
            <p class="text-2xl mt-2">de satisfaction client</p>
          </div>
          <div>
            <p class=" text-6xl">+15</p>
            <p class="text-2xl mt-2">projets réalisés</p>
          </div>
        </div>

      </div>
    </div>

    <div class="bg-gray-100">
      <div class=" max-w-[1200px] px-4 mx-auto pt-[65px] pb-[65px]">
        <div class=" flex-1/2 text-[#4B2F00] text-justify">
          <h2 class="uppercase font-black text-[27px] mb-4">
            l'equipe
          </h2>

          <div class=" flex flex-col gap-3 lg:flex-row">
            <div class="lg:flex-1/3">
              GOHZE est une jeune entreprise fondée par 4 jeunes ingénieurs de Polytechnique de Yaoundé. Derrière ce noyau dur se trouve une équipe dynamique hautement qualifiée et prête à relever tous les défis.
              <br>
              Contactez-nous, confiez-nous votre rêve et nous faisons le reste !!!
            </div>

            <div class="lg:flex-2/3 grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 justify-center gap-4 flex-wrap">
              <teamCard class=" flex-1" v-for="team in teams" :img="team.img" :name="team.name" :rule="team.rule"></teamCard>
            </div>

          </div>
        </div>
      </div>
    </div>

    <div class=" my-[65px]">
      <div class=" max-w-[1200px] px-4 mx-auto">
        <h2 class="uppercase font-black text-center text-[27px] mb-4">
          Quelques clients et partenaires qui nous ont fait confiance en Afrique et au-delà
        </h2>

        <Carousel v-bind="config">
          <Slide v-for="n in 6" :key="n">
            <img src="@/assets/iziway.webp" alt="image" />
          </Slide>

          <template #addons>
            <Navigation />
          </template>
        </Carousel>

      </div>

    </div>
  
  </div>

</template>