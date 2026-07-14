<template>
  <div class=" min-h-screen text-white">

    <!-- Section Présentation -->
    <section class="flex flex-col lg:flex-row items-center justify-center gap-8 lg:gap-14 max-w-5xl mx-auto px-4 py-16">
      <div class="relative shadow-2xl shadow-indigo-600/40 rounded-2xl overflow-hidden shrink-0 w-full max-w-sm md:max-w-md lg:max-w-sm xl:max-w-md">
        <img class="w-full h-auto object-cover rounded-2xl"
          src="/public/cv_kouli.png"
          alt="Photo de profil">
      </div>

      <div class="text-sm max-w-xl text-center lg:text-left">
        <h1 class="text-2xl md:text-3xl font-semibold text-slate-100 dark:text-white">À propos de moi...</h1>
        <div class="w-24 h-[3px] rounded-full bg-gradient-to-r from-indigo-600 to-[#DDD9FF] mx-auto lg:mx-0 mt-2"></div>

        <p class="mt-6 text-base md:text-lg leading-relaxed text-slate-300 dark:text-gray-300">
          Développeur Full-Stack spécialisé dans la conception d'applications web complètes.
          J'allie expertise en architecture back-end robuste et maîtrise des interfaces utilisateur performantes
          pour livrer des solutions évolutives, fiables et orientées résultats.
          Ma mission : traduire les enjeux métiers complexes en produits numériques à forte valeur ajoutée.

        </p>
        <a
                href="/CV_JUDICAEL.pdf"
                download="CV_JUDICAEL.pdf"
                class="inline-block mt-6 bg-gradient-to-r from-indigo-600 to-[#DDD9FF] text-white font-bold py-2 px-6 rounded-full hover:from-indigo-700 hover:to-[#CCC5FF] transition-all duration-300 shadow-lg shadow-indigo-500/20 text-center"
          >
                Mon CV
          </a>
      </div>
    </section>


    <!-- Section Services -->
    <section class="py-20 max-w-6xl mx-auto px-6">
      <div class="container mx-auto">

        <div class="flex items-center justify-center lg:justify-start gap-4 mb-12">
          <Icon icon="eos-icons:service" width="45" class="shrink-0" color="cyan"/>
          <h2 class="text-3xl text-[#00e5ff] font-bold">Ce que je peux faire pour vous</h2>
        </div>

        <!-- Grille de Services -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 lg:gap-8">

          <!-- Service 01 -->
          <div class="group rounded-2xl p-8 bg-[#090d22]/40 border border-slate-800/60 hover:border-cyan-500/30  transition-all duration-300 flex flex-col justify-between min-h-[250px]">
            <div>
              <span class="text-xs font-mono text-cyan-500/80 font-bold block mb-3">01</span>
              <h3 class="text-2xl font-bold mb-3 text-slate-100 group-hover:text-white transition-colors">Sites Web & Applications</h3>
              <p class="text-slate-400 text-sm md:text-base leading-relaxed mb-6">
                  Je transforme vos idées en plateformes web fluides et performantes. Des landing pages à fort taux de conversion aux dashboards complexes,
                  je conçois des solutions sur-mesure taillées pour propulser votre business.
              </p>
            </div>
            <!-- Badges technologiques -->
            <div class="flex flex-wrap gap-2 mt-auto">
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">NestJS</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">React</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Vue.js</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Tailwind CSS</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">HTML/CSS</span>
            </div>
          </div>

          <!-- Service 02 -->
          <div class="group rounded-2xl p-8 bg-[#090d22]/40 border border-slate-800/60 hover:border-cyan-500/30 transition-all duration-300 flex flex-col justify-between min-h-[250px]">
            <div>
              <span class="text-xs font-mono text-cyan-500/80 font-bold block mb-3">02</span>
              <h3 class="text-2xl font-bold mb-3 text-slate-100 group-hover:text-white transition-colors">API & Backend</h3>
              <p class="text-slate-400 text-sm md:text-base leading-relaxed mb-6">
              Conception d'architectures serveurs robustes, d'API sécurisées et de bases de données optimisées pour garantir la stabilité et la croissance sans limites de vos plateformes.
              </p>
            </div>
            <!-- Badges technologiques -->
            <div class="flex flex-wrap gap-2 mt-auto">
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">NestJS</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Laravel</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">MySQL</span>
            </div>
          </div>

          <!-- Service 03 -->
          <div class="group rounded-2xl p-8 bg-[#090d22]/40 border border-slate-800/60 hover:border-cyan-500/30 transition-all duration-300 flex flex-col justify-between min-h-[250px]">
            <div>
              <span class="text-xs font-mono text-cyan-500/80 font-bold block mb-3">03</span>
              <h3 class="text-2xl font-bold mb-3 text-slate-100 group-hover:text-white transition-colors">E-commerce & Marketing</h3>
              <p class="text-slate-400 text-sm md:text-base leading-relaxed mb-6">
                Conception de boutiques en ligne fluides, stratégies de conversion, SEO local et optimisation du parcours client pour maximiser vos ventes.
              </p>
            </div>
            <!-- Badges technologiques -->
            <div class="flex flex-wrap gap-2 mt-auto">
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">E-commerce</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">SEO</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Digital Strategy</span>
            </div>
          </div>

          <!-- Service 04 -->
          <div class="group rounded-2xl p-8 bg-[#090d22]/40 border border-slate-800/60 hover:border-cyan-500/30 transition-all duration-300 flex flex-col justify-between min-h-[250px]">
            <div>
              <span class="text-xs font-mono text-cyan-500/80 font-bold block mb-3">04</span>
              <h3 class="text-2xl font-bold mb-3 text-slate-100 group-hover:text-white transition-colors">Interfaces UI/UX </h3>
              <p class="text-slate-400 text-sm md:text-base leading-relaxed mb-6">
                Je crée des designs interactifs qui captivent dès le premier regard. En alliant esthétique moderne, micro-animations fluides et ergonomie intuitive,
                je conçois des interfaces pensées pour le confort et l'engagement de vos utilisateurs.
            </p>
            </div>
            <!-- Badges technologiques -->
            <div class="flex flex-wrap gap-2 mt-auto">
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Bootstrap</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Tailwind CSS</span>
              <span class="text-xs font-mono bg-cyan-500/5 text-cyan-400/80 border border-cyan-500/10 px-3 py-1 rounded">Figma</span>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- section Intérêts Personnels -->

    <section class="bg-animated cyber-grid py-16 relative overflow-hidden max-w-6xl mx-auto px-4">
      <div class="container mx-auto">
        <!-- <h2 class="text-3xl text-[#00e5ff] font-bold mb-12 text-center lg:text-left">Intérêts personnels</h2> -->
        <div class="flex items-center justify-center lg:justify-start gap-4 mb-12">
          <Icon icon="ic:outline-interests" width="45" class="shrink-0" color="cyan"/>
          <h2 class="text-3xl text-[#00e5ff] font-bold">Intérêts personnels</h2>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

          <!-- Codage -->
          <div class="feature-card rounded-lg p-6 bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-500/30 transition-all duration-300 shadow-md flex flex-col" style="animation-delay: 0.2s;">
            <div class="text-4xl mb-4 text-pink-500">
              <Icon icon="streamline-kameleon-color:windows-coding-duo" width="36" />
            </div>
            <h3 class="text-xl font-bold mb-2 text-white">Codage & Tech</h3>
            <p class="text-slate-300 text-sm leading-relaxed">Passionné par le développement d'architectures propres, l'intégration d'API et la résolution de problématiques logicielles complexes.</p>
          </div>

          <!-- Marketing -->
          <div class="feature-card rounded-lg p-6 bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-500/30 transition-all duration-300 shadow-md flex flex-col" style="animation-delay: 0.4s;">
            <div class="text-4xl mb-4 text-cyan-400">
              <Icon icon="lsicon:marketing-filled" width="36" />
            </div>
            <h3 class="text-xl font-bold mb-2 text-white">Marketing Digital</h3>
            <p class="text-slate-300 text-sm leading-relaxed">Analyse des tendances du marché et conception de stratégies e-commerce visant à maximiser la visibilité et l'impact des produits.</p>
          </div>

          <!-- Community Manager -->
          <div class="feature-card rounded-lg p-6 bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-500/30 transition-all duration-300 shadow-md flex flex-col" style="animation-delay: 0.6s;">
            <div class="text-4xl mb-4 text-purple-500">
              <Icon icon="flat-color-icons:manager" width="36" />
            </div>
            <h3 class="text-xl font-bold mb-2 text-white">Gestion de Communauté</h3>
            <p class="text-slate-300 text-sm leading-relaxed">Création de contenus visuels attrayants et fédération d'audiences engagées autour d'identités de marque fortes.</p>
          </div>

          <!-- Business -->
          <div class="feature-card rounded-lg p-6 bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-500/30 transition-all duration-300 shadow-md flex flex-col" style="animation-delay: 0.8s;">
            <div class="text-4xl mb-4 text-green-400">
              <Icon icon="mdi:business-outline" width="36" />
            </div>
            <h3 class="text-xl font-bold mb-2 text-white">Entrepreneuriat</h3>
            <p class="text-slate-300 text-sm leading-relaxed">Développement d'idées d'affaires innovantes, gestion d'e-boutiques et valorisation de projets commerciaux de bout en bout.</p>
          </div>

          <!-- Communication -->
          <div class="feature-card rounded-lg p-6 bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-500/30 transition-all duration-300 shadow-md flex flex-col" style="animation-delay: 1s;">
            <div class="text-4xl mb-4 text-yellow-400">
              <Icon icon="hugeicons:marketing" width="36" />
            </div>
            <h3 class="text-xl font-bold mb-2 text-white">Communication</h3>
            <p class="text-slate-300 text-sm leading-relaxed">Élaboration d'identités visuelles et rédaction de messages clairs pour valoriser les initiatives numériques et professionnelles.</p>
          </div>

        </div>
      </div>
    </section>

    <!-- Section Parcours Académique -->
    <section class="py-16 max-w-6xl mx-auto px-4">
        <div class="flex items-center justify-center lg:justify-start gap-4 mb-12">
          <Icon icon="noto:graduation-cap" width="45" class="shrink-0" />
          <h2 class="text-3xl text-[#00e5ff] font-bold">Mon parcours académique</h2>
        </div>

      <div class="w-full max-w-3xl mx-auto">
        <div class="space-y-8 relative before:absolute before:inset-0 before:ml-5 before:-translate-x-px md:before:ml-[8.75rem] md:before:translate-x-0 before:h-full before:w-0.5 before:bg-gradient-to-b before:from-transparent before:via-slate-700 before:to-transparent">

          <!-- Item 1 -->
          <div class="relative">
            <div class="md:flex items-center md:space-x-4 mb-3">
              <div class="flex items-center space-x-4 md:space-x-2 md:space-x-reverse">
                <div class="flex items-center justify-center w-10 h-10 rounded-full bg-white shadow-xl md:order-1 border border-cyan-500/20">
                  <Icon icon="mdi:code" width="22" class="text-gray-900"/>
                </div>
                <time class="sacramento-regular text-xl text-[#00e5ff] md:w-28 md:text-right block">2025-2026</time>
              </div>
            </div>
            <div class="p-5 rounded-2xl border border-custom shadow-lg ml-14 md:ml-44 hover:border-custom transition-colors">
              <h3 class="text-lg font-bold text-white mb-1">Développeur Full-Stack</h3>
              <p class="text-sm text-cyan-400 font-medium mb-2">We.Code — Formation Intensive</p>
              <p class="text-sm text-slate-300 leading-relaxed">
                +1000 heures de code intensives axées sur la pratique. Conception d'applications web modernes, gestion des bases de données et déploiement de solutions d'envergure.
              </p>

            </div>
          </div>

          <!-- Item 2 -->
          <div class="relative">
            <div class="md:flex items-center md:space-x-4 mb-3">
              <div class="flex items-center space-x-4 md:space-x-2 md:space-x-reverse">
                <div class="flex items-center justify-center w-10 h-10 rounded-full bg-white shadow-xl md:order-1 border border-cyan-500/20">
                  <Icon icon="maki:college" width="22" class="text-gray-900"/>
                </div>
                <time class="sacramento-regular text-xl text-[#00e5ff] md:w-28 md:text-right block">2024-2025</time>
              </div>
            </div>
            <div class="p-5 rounded-2xl border border-custom shadow-lg ml-14 md:ml-44 border-custom transition-colors">
              <h3 class="text-lg font-bold text-white mb-1">Licence en E-commerce & Marketing Digital</h3>
              <p class="text-sm text-cyan-400 font-medium mb-2">Université Virtuelle de Côte d'Ivoire (UVCI)</p>
              <p class="text-sm text-slate-300 leading-relaxed">
                Spécialisation en stratégies d'acquisition, SEO, gestion de projets digitaux et analyse de données. Une vision business qui complète parfaitement mon profil de développeur.
              </p>

            </div>
          </div>

          <!-- Item 3 -->
          <div class="relative">
            <div class="md:flex items-center md:space-x-4 mb-3">
              <div class="flex items-center space-x-4 md:space-x-2 md:space-x-reverse">
                <div class="flex items-center justify-center w-10 h-10 rounded-full bg-white shadow-xl md:order-1 border border-cyan-500/20">
                  <Icon icon="map:university" width="22" class="text-gray-900"/>
                </div>
                <time class="sacramento-regular text-xl text-[#00e5ff] md:w-28 md:text-right block">2021-2022</time>
              </div>
            </div>
            <div class="p-5 rounded-2xl border border-custom shadow-lg ml-14 md:ml-44 hover:border-custom transition-colors">
             <h3 class="text-lg font-bold text-white mb-1">Baccalauréat (BAC)</h3>
              <p class="text-sm text-cyan-400 font-medium mb-2">Lycée Moderne de Bondoukou</p>
              <p class="text-sm text-slate-300">
                Diplôme de fin d'études secondaires.
              </p>

            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- Footer -->
    <FooterView/>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue'
import FooterView from './FooterView.vue';
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Sacramento&display=swap');

.sacramento-regular {
  font-family: "Sacramento", cursive;
  font-weight: 400;
  font-style: italic;
}


/* Gradient text */
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}


/* Animated gradient border */
.gradient-border {
    position: relative;
    background: linear-gradient(#0a0a0a, #0a0a0a) padding-box,
                linear-gradient(135deg, #667eea, #764ba2, #f093fb) border-box;
    border: 2px solid transparent;
}
</style>
