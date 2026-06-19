<template>
  <section class="relative flex flex-col items-center bg-black text-white pb-16 pt-8 bg-[url(https://raw.githubusercontent.com/prebuiltui/prebuiltui/main/assets/hero/bg-gradient-3.svg)] bg-center bg-cover">

    <nav class="flex items-center border mx-4 max-md:w-full max-md:justify-between border-slate-700 px-6 py-4 rounded-full text-white text-sm">
      <a href="">
        <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" fill="currentColor" color="blue" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1.114 8.063V7.9c1.005-.102 1.497-.615 1.497-1.6V4.503c0-1.094.39-1.538 1.354-1.538h.273V2h-.376C2.25 2 1.49 2.759 1.49 4.352v1.524c0 1.094-.376 1.456-1.49 1.456v1.299c1.114 0 1.49.362 1.49 1.456v1.524c0 1.593.759 2.352 2.372 2.352h.376v-.964h-.273c-.964 0-1.354-.444-1.354-1.538V9.663c0-.984-.492-1.497-1.497-1.6M14.886 7.9v.164c-1.005.103-1.497.616-1.497 1.6v1.798c0 1.094-.39 1.538-1.354 1.538h-.273v.964h.376c1.613 0 2.372-.759 2.372-2.352v-1.524c0-1.094.376-1.456 1.49-1.456v-1.3c-1.114 0-1.49-.362-1.49-1.456V4.352C14.51 2.759 13.75 2 12.138 2h-.376v.964h.273c.964 0 1.354.444 1.354 1.538V6.3c0 .984.492 1.497 1.497 1.6M7.5 11.5V9.207l-1.621 1.621-.707-.707L6.792 8.5H4.5v-1h2.293L5.172 5.879l.707-.707L7.5 6.792V4.5h1v2.293l1.621-1.621.707.707L9.208 7.5H11.5v1H9.207l1.621 1.621-.707.707L8.5 9.208V11.5z"/>
        </svg>
      </a>

      <div class="hidden md:flex items-center gap-6 ml-7">
        <a href="#" class="relative overflow-hidden h-6 group">
          <span class="block group-hover:-translate-y-full transition-transform duration-300">Home</span>
          <span class="block absolute top-full left-0 group-hover:translate-y-[-100%] transition-transform duration-300">Home</span>
        </a>
        <a href="#" class="relative overflow-hidden h-6 group">
          <span class="block group-hover:-translate-y-full transition-transform duration-300">About</span>
          <span class="block absolute top-full left-0 group-hover:translate-y-[-100%] transition-transform duration-300">About</span>
        </a>
        <a href="#" class="relative overflow-hidden h-6 group">
          <span class="block group-hover:-translate-y-full transition-transform duration-300">Éducation</span>
          <span class="block absolute top-full left-0 group-hover:translate-y-[-100%] transition-transform duration-300">Éducation</span>
        </a>
        <a href="#" class="relative overflow-hidden h-6 group">
          <span class="block group-hover:-translate-y-full transition-transform duration-300">Réalisations</span>
          <span class="block absolute top-full left-0 group-hover:translate-y-[-100%] transition-transform duration-300">Réalisations</span>
        </a>
        <a href="#" class="relative overflow-hidden h-6 group">
          <span class="block group-hover:-translate-y-full transition-transform duration-300">Compétences</span>
          <span class="block absolute top-full left-0 group-hover:translate-y-[-100%] transition-transform duration-300">Compétences</span>
        </a>
      </div>

      <div class="hidden ml-14 md:flex items-center gap-4">
        <button class="bg-white hover:shadow-[0px_0px_30px_14px] shadow-[0px_0px_30px_7px] hover:shadow-white/50 shadow-white/50 text-black px-4 py-2 rounded-full text-sm font-medium hover:bg-slate-100 transition duration-300">
          Contact
        </button>
      </div>

      <!-- Hamburger -->
      <button @click="toggleMenu" class="md:hidden text-gray-600">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>

      <!-- Menu mobile -->
      <div :class="['absolute top-0 left-0 bg-black w-full h-full flex-col items-center justify-center gap-4 text-base', isMenuOpen ? 'flex' : 'hidden']">
        <a @click="closeMenu" class="hover:text-indigo-600" href="#">Home</a>
        <a @click="closeMenu" class="hover:text-indigo-600" href="#">About</a>
        <a @click="closeMenu" class="hover:text-indigo-600" href="#">Éducation</a>
        <a @click="closeMenu" class="hover:text-indigo-600" href="#">Réalisations</a>
        <a @click="closeMenu" class="hover:text-indigo-600" href="#">Compétences</a>
        <button @click="closeMenu" class="bg-white hover:shadow-[0px_0px_30px_14px] shadow-[0px_0px_30px_7px] hover:shadow-white/50 shadow-white/50 text-black px-4 py-2 rounded-full text-sm font-medium hover:bg-slate-100 transition duration-300">
          Contact
        </button>
      </div>
    </nav>

    <!-- Hero content — identique à ton original -->
    <div class="flex items-center gap-2 border border-white/15 rounded-full px-4 py-2 text-sm mt-24">
      <p>Salut je suis Judicael Kouly</p>
      <!-- <a href="#" class="flex items-center gap-1 font-medium">
        Read more
        <svg class="mt-0.5" width="19" height="19" viewBox="0 0 19 19" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3.959 9.5h11.083m0 0L9.501 3.96m5.541 5.54-5.541 5.542" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
        </svg>
      </a> -->
    </div>

    <h1 class="md:text-6xl text-center font-semibold max-w-3xl mt-5 bg-gradient-to-r from-white to-[#748298] text-transparent bg-clip-text">
      A Propos de moi
    </h1>
    <p class="text-slate-300 md:text-base line-clamp-8 max-md:px-2 text-center max-w-2xl mt-3">
      <span>Bienvenue dans mon univers numérique</span> <br>

     Je suis développeur Web, spécialisé dans le développement backend avec un peu de travail en frontend également.
     J'ai aussi de l'expérience en production avec les technologies C++, C#, Go et Python.
    Ce parcours diversifié me permet de m'adapter à une large gamme de besoins de projets,
    qu'il s'agisse de créer des API évolutives, d'améliorer les performances système ou de participer à des solutions full-stack.
    Je suis impatient de collaborer avec vous !
    </p>

    <div class="flex items-center gap-2 border border-white/15 rounded-full px-4 py-2 text-sm mt-24">
      <p>Intérêts personnels</p>

    </div>

    <div class="mt-12 flex max-md:overflow-x-auto gap-6 max-w-4xl w-full pb-6">
      <img class="w-36 h-44 rounded-lg hover:-translate-y-1 transition duration-300 object-cover flex-shrink-0" src="https://images.unsplash.com/flagged/photo-1573740144655-bbb6e88fb18a?q=80&w=735&auto=format&fit=crop" alt="" />
      <img class="w-36 h-44 rounded-lg hover:-translate-y-1 transition duration-300 object-cover flex-shrink-0" src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?q=80&w=687&auto=format&fit=crop" alt="" />
      <img class="w-36 h-44 rounded-lg hover:-translate-y-1 transition duration-300 object-cover flex-shrink-0" src="https://images.unsplash.com/photo-1560250097-0b93528c311a?q=80&w=687&auto=format&fit=crop" alt="" />
      <img class="w-36 h-44 rounded-lg hover:-translate-y-1 transition duration-300 object-cover flex-shrink-0" src="https://images.unsplash.com/photo-1546961329-78bef0414d7c?q=80&w=687&auto=format&fit=crop" alt="" />
      <img class="w-36 h-44 rounded-lg hover:-translate-y-1 transition duration-300 object-cover flex-shrink-0" src="https://images.unsplash.com/photo-1639149888905-fb39731f2e6c?q=80&w=764&auto=format&fit=crop" alt="" />
    </div>




  </section>

<!-- component -->
<!-- This is an example component -->
<link href="https://unpkg.com/pattern.css" rel="stylesheet">

<!-- un composant à recuperer -->

<!-- <div>
    <section class="text-gray-200 bg-gray-900">
        <div class="max-w-6xl mx-auto px-5 py-24 ">
          <div class="text-center mb-20">
            <h1 class=" title-font  mb-4 text-4xl font-extrabold leading-10 tracking-tight sm:text-5xl sm:leading-none md:text-6xl">Compétences</h1>
            <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">L'informatique est vaste et les langages naissent presque à tout moment, je fais tout mon possible pour être à la hauteur afin de répondre au besoin de mes clients et d'apporter de l'aide aux nouveaux développeurs.</p>
            <div class="flex mt-6 justify-center">
              <div class="w-16 h-1 rounded-full bg-indigo-500 inline-flex"></div>
            </div>
          </div>
          <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4 ">
            <div class="p-10 md:w-1/3 md:mb-0 mb-6 flex flex-col ">
              <div class="pattern-dots-md gray-light">
                <div class="rounded bg-gray-800 p-4 transform translate-x-6 -translate-y-6  "  >
                  <div class="w-10 h-10 inline-flex items-center justify-center rounded-full bg-green-100 text-green-500 mb-5 flex-shrink-0 p-2">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"></path></svg>                </div>
                  <div class="flex-grow ">
                    <h2 class=" text-xl title-font font-medium mb-3">Webdesign</h2>
                    <p class="leading-relaxed text-sm text-justify">Donner du goût ? de la couleur aux applications, je le fais afin de rendre vos sites attrayants ?. Avant de devenir webdesigner, depuis tout petit j'étais déjà familier à la couleur et du dessin.</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="p-10 md:w-1/3 md:mb-0 mb-6 flex flex-col ">
              <div class="pattern-dots-md gray-light">
                <div class="rounded bg-gray-800 p-4 transform translate-x-6 -translate-y-6 ">
                  <div class="w-10 h-10 inline-flex items-center justify-center rounded-full bg-blue-100 text-blue-500 mb-5 flex-shrink-0">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path></svg>
                  </div>
                  <div class="flex-grow">
                    <h2 class=" text-xl title-font font-medium mb-3">Intégration web</h2>
                    <p class="leading-relaxed text-sm text-justify">
                    Donner du goût ? de la couleur aux applications, je le fais afin de rendre vos sites attrayants ?. Avant de devenir webdesigner, depuis tout petit j'étais déjà familier à la couleur et du dessin.
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="p-10 md:w-1/3 md:mb-0 mb-6 flex flex-col ">
              <div class="pattern-dots-md gray-light">
                <div class="rounded bg-gray-800 p-4 transform translate-x-6 -translate-y-6 ">
                  <div class="w-10 h-10 inline-flex items-center justify-center rounded-full bg-yellow-100 text-yellow-500 mb-5 flex-shrink-0">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4"></path></svg>
                  </div>
                  <div class="flex-grow">
                    <h2 class=" text-xl title-font font-medium mb-3">Developpement Back-end</h2>
                    <p class="leading-relaxed text-sm text-justify">
                     Grâce à Php et ces frameworks (Larave, Symfoni, Slim), je peux vous réaliser un site dynamique c'est-à-dire qui interagie avec votre base de données ?. Nous pouvons essayer.
                    </p>
                  </div>
                </div>
        </div>
    </section>
</div> -->

</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value
}

function closeMenu() {
  isMenuOpen.value = false
}
</script>
<style lang="scss">


</style>




