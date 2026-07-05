<template>
  <div class="bg-gray-900 min-h-screen flex items-center justify-center p-4 overflow-hidden relative font-sans">
    <div ref="starsContainer" class="fixed inset-0 pointer-events-none"></div>

    <div class="error-container relative z-10 text-center max-w-lg mx-auto px-4">

      <div class="relative space-animation mb-6">
        <svg class="w-36 h-36 mx-auto" viewBox="0 0 100 100">
          <ellipse cx="50" cy="40" rx="30" ry="10" fill="#4F46E5"/>
          <circle cx="50" cy="35" r="20" fill="#818CF8"/>
          <ellipse cx="50" cy="30" rx="10" ry="5" fill="#C7D2FE"/>
          <path class="ufo-beam" d="M40 40 L30 80 L70 80 L60 40" fill="rgba(79, 70, 229, 0.2)"/>
        </svg>
      </div>

      <h1 class="text-7xl font-extrabold text-white mb-4 tracking-wider space-animation">
        4<span class="inline-block portal text-indigo-400 mx-1">0</span>3
      </h1>

      <h2 class="text-2xl font-bold text-blue-200 mb-3">Accès Restreint / Code Source Privé</h2>
      <p class="text-gray-400 mb-8 leading-relaxed text-sm md:text-base">
        Le code source de ce projet est actuellement hébergé sur un dépôt privé pour des raisons de confidentialité ou de propriété intellectuelle.
        Si vous souhaitez en savoir plus sur l'architecture technique ou obtenir une démonstration guidée, n'hésitez pas à me contacter !
      </p>

      <div class="space-y-6">
        <div class="flex flex-col sm:flex-row justify-center items-center gap-4">
          <router-link
            to="/"
            class="w-full sm:w-auto px-6 py-3 bg-indigo-600 text-white font-medium rounded-full hover:bg-indigo-700 transform hover:-translate-y-0.5 transition-all duration-200 shadow-lg shadow-indigo-600/30 text-center"
          >
            Retour au portfolio
          </router-link>

          <button
            @click="goBack"
            class="w-full sm:w-auto px-6 py-3 bg-gray-800 text-gray-200 font-medium rounded-full border border-gray-700 hover:bg-gray-700 transform hover:-translate-y-0.5 transition-all duration-200 text-center"
          >
            Page précédente
          </button>
        </div>
      </div>

      <div class="mt-12 text-gray-600 cursor-pointer hover:text-gray-500 transition-colors duration-200">
        <p class="text-xs">Un peu perdu dans le vide spatial ? Pressez la touche 'Espace' pour illuminer le cosmos.</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();
const starsContainer = ref(null);
let meteorInterval = null;

// Navigation retour
const goBack = () => {
  router.back();
};

// Easter Egg : Changement de background au clic sur Espace
const handleKeyDown = (e) => {
  if (e.code === 'Space') {
    e.preventDefault(); // Empêche le scroll de la page
    document.body.style.backgroundColor = `hsl(${Math.random() * 360}, 50%, 15%)`;
    setTimeout(() => {
      document.body.style.backgroundColor = '';
    }, 500);
  }
};

onMounted(() => {
  // Génération des étoiles en arrière-plan
  if (starsContainer.value) {
    for (let i = 0; i < 80; i++) {
      const star = document.createElement('div');
      star.className = 'star-dot';
      star.style.left = `${Math.random() * 100}%`;
      star.style.top = `${Math.random() * 100}%`;

      const size = Math.random() * 3;
      star.style.width = `${size}px`;
      star.style.height = `${size}px`;
      star.style.setProperty('--duration', `${Math.random() * 3 + 1.5}s`);

      starsContainer.value.appendChild(star);
    }
  }

  // Génération des météores à intervalles réguliers
  meteorInterval = setInterval(() => {
    const meteor = document.createElement('div');
    meteor.className = 'meteor-line';
    meteor.style.top = `${Math.random() * 60}%`;
    meteor.style.left = '100%';
    document.body.appendChild(meteor);
    setTimeout(() => meteor.remove(), 2000);
  }, 4000);

  // Écouteur du clavier
  window.addEventListener('keydown', handleKeyDown);
});

onUnmounted(() => {
  // Nettoyage des événements et intervalles pour optimiser les performances
  clearInterval(meteorInterval);
  window.removeEventListener('keydown', handleKeyDown);
});
</script>

<style scoped>
/* Animations existantes adaptées et encapsulées (scoped) */
.space-animation {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
}

.ufo-beam {
  animation: beam 2s ease-in-out infinite;
  transform-origin: top;
}

@keyframes beam {
  0%, 100% { transform: scaleY(0.8); opacity: 0.2; }
  50% { transform: scaleY(1.1); opacity: 0.6; }
}

.portal {
  animation: portal-spin 12s linear infinite;
}

@keyframes portal-spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

/* Styles injectés dynamiquement pour éviter les conflits globaux */
:deep(.star-dot) {
  position: absolute;
  background: white;
  border-radius: 50%;
  animation: twinkle var(--duration) ease-in-out infinite;
  opacity: 0;
}

@keyframes twinkle {
  0%, 100% { opacity: 0; }
  50% { opacity: 0.8; }
}

:deep(.meteor-line) {
  position: absolute;
  width: 40px;
  height: 1px;
  background: linear-gradient(90deg, #ffffff, transparent);
  animation: meteor-move 2s linear forwards;
  pointer-events: none;
  z-index: 1;
}

@keyframes meteor-move {
  0% { transform: translate(0, 0) rotate(-25deg); opacity: 1; }
  100% { transform: translate(-100vw, 50vh) rotate(-25deg); opacity: 0; }
}
</style>
