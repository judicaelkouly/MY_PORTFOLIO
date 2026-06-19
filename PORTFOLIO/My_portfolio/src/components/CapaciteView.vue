<template>


<div class="mb-25">

  <div class="text-center mb-20">
            <h1 class="mb-4 text-4xl text-[#00e5ff] font-extrabold leading-10 tracking-tight sm:text-5xl sm:leading-none md:text-6xl">Compétences</h1>
            <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">L'informatique est vaste et les langages naissent presque à tout moment, je fais tout mon possible pour être à la hauteur afin de répondre au besoin de mes clients et d'apporter de l'aide aux nouveaux développeurs.</p>
            <div class="flex mt-6 justify-center">
              <div class="w-16 h-1 rounded-full bg-indigo-500 inline-flex"></div>
            </div>
  </div>
<!--
  Ajustements de la grille :
  - Ajout d'un effet perspective globale.
  - Ajout de styles personnalisés en bas pour l'effet d'apparition fluide au scroll.
-->
<div class="w-full max-w-6xl mx-auto px-4 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 justify-items-center gap-y-16 gap-x-10 mt-10 mb-5 perspective-container">

  <!-- -----------Card 1------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 1;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="ic:baseline-web" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">Conception de websites</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je suis en mesure de concrétiser vos idées les plus brillantes et de les matérialiser.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

  <!-- -----------Card 2------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 2;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="tdesign:data-base-filled" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">Gestion de base de données</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je suis en mesure de gérer vos bases de données avec efficacité et efficience.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

  <!-- -----------Card 3------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 3;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="hugeicons:api" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">APIs REST</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je suis en mesure de développer des services API.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

  <!-- -----------Card 4------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 1;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="fa-brands:teamspeak" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">Community Management</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je peux administrer vos communautés en ligne en valorisant l'image et la réputation de votre entreprise.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

  <!-- -----------Card 5------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 2;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="lsicon:marketing-outline" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">Agent marketing</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je suis en mesure de réaliser une étude de marché.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

  <!-- -----------Card 6------------- -->
  <div
    class="scroll-animate group cursor-pointer transform transition-all duration-500 hover:scale-105 hover:-rotate-1 w-full max-w-[350px]"
    style="--delay: 3;"
  >
    <div
      class="text-white rounded-3xl border border-cyan-500/20 bg-gradient-to-tr from-[#0F0F0F] to-[#0B0B0B] shadow-2xl duration-700 z-10 relative backdrop-blur-xl hover:border-cyan-400/40 overflow-hidden hover:shadow-cyan-500/10 hover:shadow-3xl w-full min-h-[400px]"
    >
      <div class="absolute inset-0 z-0 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/5 to-cyan-400/10 opacity-40 group-hover:opacity-60 transition-opacity duration-500"></div>
        <div class="absolute -bottom-20 -left-20 w-48 h-48 rounded-full bg-gradient-to-tr from-cyan-500/10 to-transparent blur-3xl opacity-30 group-hover:opacity-50 transform group-hover:scale-110 transition-all duration-700 animate-bounce delay-500"></div>
        <div class="absolute top-10 left-10 w-16 h-16 rounded-full bg-cyan-500/5 blur-xl animate-ping"></div>
        <div class="absolute bottom-16 right-16 w-12 h-12 rounded-full bg-cyan-500/5 blur-lg animate-ping delay-1000"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-cyan-500/5 to-transparent transform -skew-x-12 translate-x-full group-hover:translate-x-[-200%] transition-transform duration-1000"></div>
      </div>

      <div class="p-8 relative z-10">
        <div class="flex flex-col items-center text-center">
          <div class="relative mb-6">
            <div class="absolute inset-0 rounded-full border-2 border-cyan-500/20 animate-ping"></div>
            <div class="absolute inset-0 rounded-full border border-cyan-500/10 animate-pulse delay-500"></div>
            <div class="p-6 rounded-full backdrop-blur-lg border border-cyan-500/20 bg-gradient-to-br from-black/80 to-gray-900/60 shadow-2xl transform group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 hover:shadow-cyan-500/20">
              <div class="transform group-hover:rotate-180 transition-transform duration-700 text-[#00e5ff]">
                <Icon icon="fluent:people-community-24-filled" width="26" />
              </div>
            </div>
          </div>
          <div class="mb-4 transform group-hover:scale-105 transition-transform duration-300">
            <p class="text-2xl font-bold bg-gradient-to-r from-cyan-400 via-[#00e5ff] to-cyan-400 bg-clip-text text-transparent">Collaboratif</p>
          </div>
          <div class="space-y-1 max-w-sm">
            <p class="text-white text-base transform group-hover:scale-105 transition-transform duration-300">Je suis en mesure de coopérer avec les autres sur un projet.</p>
          </div>
          <div class="mt-6 w-1/3 h-0.5 bg-gradient-to-r from-transparent via-[#00e5ff] to-transparent rounded-full transform group-hover:w-1/2 group-hover:h-1 transition-all duration-500 animate-pulse"></div>
          <div class="flex space-x-2 mt-4 opacity-60 group-hover:opacity-100 transition-opacity duration-300">
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-100"></div>
            <div class="w-2 h-2 bg-[#00e5ff] rounded-full animate-bounce delay-200"></div>
          </div>
        </div>
      </div>
      <div class="absolute top-0 left-0 w-20 h-20 bg-gradient-to-br from-cyan-500/10 to-transparent rounded-br-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
      <div class="absolute bottom-0 right-0 w-20 h-20 bg-gradient-to-tl from-cyan-500/10 to-transparent rounded-tl-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    </div>
  </div>

</div>



</div>

 <h1 class=" mb-10 text-4xl text-[#00e5ff] font-extrabold leading-10 tracking-tight sm:text-5xl sm:leading-none md:text-6xl">Stack Backend</h1>


<div class="mb-10 flex">
  <div class="relative w-full">
    <div class="relative grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 ">

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="logos:nodejs-icon" width="40" />
          Node.js
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="catppuccin:php" width="40" />
          PHP 8+
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:laravel" width="40" />
          Laravel
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:nestjs" width="40" />
          Nest.js
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:mysql" width="40" />
          MySQL
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:mongodb" width="40" />
          MongoDB
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

    </div>
  </div>
</div>

 <h1 class=" mb-10 text-4xl text-[#00e5ff] font-extrabold leading-10 tracking-tight sm:text-5xl sm:leading-none md:text-6xl">Stack Frontend</h1>


<div class=" mb-20">
  <div class="relative w-full">
    <div class="relative grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 ">

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="logos:html-5" width="40" />
          HTML 5
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="logos:react" width="40" />
          React
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:vuejs" width="40" />
          Vue.js
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:javascript" width="40" />
          Javascript
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="logos:bootstrap" width="40" />
          Bootstrap
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="devicon:tailwindcss" width="40" />
          Tailwind
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>
      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="skill-icons:css" width="40" />
          CSS 3
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>

      <div class="p-5 border border-custom rounded-lg flex items-center justify-between space-x-4">
        <p class="font-semibold flex items-center gap-2 shrink-0">
          <Icon icon="logos:nextjs-icon" width="40" />
          Next.js
        </p>
        <div class="h-2 flex-1 bg-gray-300 rounded"></div>
        <div class="w-8 h-8 rounded-full bg-green-300 shrink-0"></div>
      </div>
    </div>
  </div>
</div>
<FooterView/>
</template>


<script setup>
import { Icon } from '@iconify/vue'
import FooterView from './FooterView.vue';

</script>

<style scoped>
  /* Ajoute un effet de perspective 3D sur l'affichage */
  .perspective-container {
    perspective: 1200px;
  }

  /* Configuration de l'animation déclenchée par le scroll */
  .scroll-animate {
    opacity: 0;
    transform: translateY(60px) scale(0.9) rotateX(10deg);
    animation: revealLinear linear both;
    animation-timeline: view();
    animation-range: entry 5% cover 30%;
  }

  @keyframes revealLinear {
    to {
      opacity: 1;
      transform: translateY(0) scale(1) rotateX(0deg);
    }
  }

  /* Fallback (sécurité) : Si le navigateur ne gère pas encore l'animation-timeline native (vieux navigateurs),
     on applique une transition CSS standard au chargement */
  @supports not (animation-timeline: view()) {
    .scroll-animate {
      opacity: 1;
      transform: none;
    }
  }
</style>
