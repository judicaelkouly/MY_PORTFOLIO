<template>
  <footer class="w-full mt-20 border-t border-custom rounded-lg backdrop-blur-xl text-slate-300">
    <div class="max-w-6xl mx-auto px-6 py-12 grid grid-cols-1 md:grid-cols-3 gap-10 items-start">

      <!-- Colonne 1 : À propos / Identité -->
      <div class="space-y-3">
        <h3 class="text-xl font-bold bg-gradient-to-r from-cyan-400 to-[#00e5ff] bg-clip-text text-transparent">
          Judicael Kouli.
        </h3>
        <p class="text-sm text-slate-400 leading-relaxed">
          Développeur Full-Stack & Solutions Digitales. Passionnée par la création d'applications web performantes, robustes et orientées business.
        </p>
      </div>

      <!-- Colonne 2 : Contact direct -->
      <div class="space-y-3">
        <h4 class="text-white font-semibold text-base">Me contacter</h4>
        <ul class="space-y-2 text-sm">
          <li class="flex items-center gap-2 hover:text-cyan-400 transition-colors">
            <Icon icon="lucide:mail" width="16" class="text-cyan-400" />
            <a href="mailto:judicael.kouli@epitech.eu">Envoyer un message</a>
          </li>
          <li class="flex items-center gap-2 text-slate-400">
            <Icon icon="lucide:map-pin" width="16" class="text-cyan-400" />
            <span>Abidjan, Côte d'Ivoire</span>
          </li>
        </ul>
      </div>

      <!-- Colonne 3 : Réseaux & Communautés -->
      <div class="space-y-3">
        <h4 class="text-white font-semibold text-base">Réseaux professionnels</h4>
        <p class="text-sm text-slate-400 mb-2">Suivez mes projets ou échangeons ensemble :</p>
        <div class="flex items-center gap-4 text-cyan-400">
          <!-- LinkedIn -->
          <a href="https://www.linkedin.com/in/kouli" target="_blank" class="p-2 rounded-lg bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-400 hover:text-white hover:-translate-y-1 transition-all duration-300 shadow-md" title="LinkedIn">
            <Icon icon="lucide:linkedin" width="20" />
          </a>
          <!-- GitHub -->
          <a href="https://github.com/judicaelkouly" target="_blank" class="p-2 rounded-lg bg-[#0d1436] border border-cyan-500/10 hover:border-cyan-400 hover:text-white hover:-translate-y-1 transition-all duration-300 shadow-md" title="GitHub">
            <Icon icon="lucide:github" width="20" />
          </a>
        </div>
      </div>

    </div>

    <!-- Ligne de Copyright finale -->
    <div class="w-full border-t border-cyan-500/5 py-6 text-center text-xs text-slate-500">
      <p>© 2026 Judicael Kouli. Tous droits réservés.</p>
    </div>
  </footer>
</template>

<script setup>
import { Icon } from '@iconify/vue'
</script>

<style scoped>
/* Ajout d'une ombre subtile au survol des liens réseaux */
a:hover {
  box-shadow: 0 0 12px rgba(0, 229, 255, 0.2);
}
</style>
