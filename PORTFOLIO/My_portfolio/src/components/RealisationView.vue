<template>
  <div class="relative font-inter antialiased min-h-screen">

    <main class="mb-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center py-12">
        <h1 class="font-extrabold text-[#00e5ff] text-4xl mb-4 tracking-tight sm:text-5xl">
          Projets académiques réalisés
        </h1>
        <div class="w-16 h-1 bg-indigo-500 mx-auto rounded-full mt-4"></div>
      </div>

      <section class="grid grid-cols-1 md:grid-cols-1 lg:grid-cols-3 justify-items-center gap-y-16 gap-x-10 mt-6 mb-12">

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/pos.png" alt="PostIt_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="devicon:vuejs" width="24"/></div>
                <div class="tech-icon"><Icon icon="skill-icons:typescript" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>

              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">Post_It</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                 <span class="font-bold">Application de Gestion de Notes</span> <br>
                  Développement complet d'une interface dynamique de gestion de notes connectée en temps réel à une API REST externe. <br>
                 <span class="font-bold">Technologies :</span>  Vue.js 3 (Composition API), TypeScript, Tailwind CSS, Axios.
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="https://github.com/judicaelkouly/Post-it_app" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16"/>
                  <span>Github</span>
                </button>
              </a>
              <a href="https://my-post-it-app-seven.vercel.app/" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16"/>
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/pos.png" alt="Yowl_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="logos:laravel" width="22"/></div>
                <div class="tech-icon"><Icon icon="devicon:vuejs" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>
                <div class="tech-icon"><Icon icon="skill-icons:css" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">YOWL</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                Application web participative et centralisée visant à décentraliser les espaces de discussion et à permettre
                aux utilisateurs de commenter n'importe quel contenu ou site web de l'Internet. <br>
                <span class="font-bold">Technologies :</span> Laravel (API), Vue.js (Frontend), SQL, GitHub. <br>
                <span class="font-bold">Fonctionnalités clés :</span>  Authentification sécurisée, système de commentaires communautaires interconnectés
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="/forbiden" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16" />
                  <span>Github</span>
                </button>
              </a>
              <a href="#" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16"/>
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/movies.png" alt="movies_project_screem" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="logos:nestjs" width="24"/></div>
                <div class="tech-icon"><Icon icon="logos:nextjs-icon" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">Gorge Movies</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                Plateforme web d'exploration, de notation et de critique de films inspirée du célèbre site Rotten Tomatoes. <br>
                <span class="font-bold">Technologies :</span> Nest.js, Next.js, Tailwind CSS, MongoDB, Git. <br>
                 <span class="font-bold">Fonctionnalités clés :</span> Authentification, gestion de favoris, filtres avancés (genres, dates), espace commentaires et
                tableau de bord administrateur (CRUD utilisateurs/films et statistiques).

                          </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="/forbiden" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16"/>
                  <span>Github</span>
                </button>
              </a>
              <a href="https://gorge-movie.vercel.app/" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16"/>
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/trel.jpeg" alt="TrellTech_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="devicon:reactnative" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">TrellTech</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
              Application mobile pour la gestion de tâches, axée sur
              la consommation d'API sécurisées de Trello et une expérience utilisateur (UI/UX) soignée. <br>
              <span class="font-bold">Technologies :</span> React Native, API Trello, OAuth2. <br>
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="/forbiden" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16"/>
                  <span>Github</span>
                </button>
              </a>
              <a href="https://expo.dev/artifacts/eas/bGbn2At4ZJ4ox7PuF2aE1j.apk" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16"/>
                  <span>Télécharger</span>
                </button>
              </a>
            </div>
          </div>
        </div>

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/myContact.jpeg" alt="MyContacts_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="devicon:vuejs" width="24"/></div>
                <div class="tech-icon"><Icon icon="skill-icons:typescript" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">MyContacts</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                Une application web moderne et sécurisée pour centraliser, rechercher et gérer ses contacts en un clic. Développée
                avec une architecture CRUD complète connectée à une API REST. <br>
                <span class="font-bold">Technologies :</span> Vue.js 3 (Composition API), TypeScript, Tailwind CSS, Axios. <br>
                <span class="font-bold">Fonctionnalités clés :</span> Authentification sécurisée, gestion des contacts (CRUD), recherche et filtrage avancé.
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="https://github.com/judicaelkouly/Contacts_app" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16"/>
                  <span>Github</span>
                </button>
              </a>
              <a href="https://my-contacts-theta.vercel.app/" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16" />
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>

        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/pos.png" alt="PostIt_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="devicon:nestjs" width="24"/></div>
                <div class="tech-icon"><Icon icon="logos:nodejs-icon" width="24"/></div>
                <div class="tech-icon"><Icon icon="selfhst:mongodb" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">My Show Time</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                Une plateforme web complète de billetterie événementielle propulsée par NestJS et MongoDB,
                intégrant une gestion fine des utilisateurs (alertes, QR codes) et un panneau d'administration basé sur les données. <br>
                <span class="font-bold">Technologies :</span> NestJS, MongoDB, Node.js. <br>
                <span class="font-bold">Fonctionnalités clés :</span> Recherche et filtres, système de favoris avec alertes, et création automatique de QR codes pour les billets.
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="/forbiden" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16" />
                  <span>Github</span>
                </button>
              </a>
              <a href="" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16" />
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>
        <div class="w-full max-w-[360px] border-2 border-cyan-500/10 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl overflow-hidden flex flex-col">
          <img src="/public/port.jpeg" alt="Portfolio_Project_image" class="w-full aspect-video object-cover" />
          <div class="px-5 py-5 flex flex-col flex-1 justify-between">
            <div>
              <div class="tech-icons">
                <div class="tech-icon"><Icon icon="devicon:vuejs" width="24"/></div>
                <div class="tech-icon"><Icon icon="devicon:tailwindcss" width="24"/></div>
                <div class="tech-icon"><Icon icon="skill-icons:css" width="24"/></div>
              </div>
              <p class="text-xl font-bold text-white truncate block capitalize mb-2">Mon Portfolio</p>
              <p class="text-gray-300 text-sm leading-relaxed mb-6">
                Vitrine numérique personnelle conçue pour présenter mes compétences techniques, mes projets réalisés et mon parcours de développeur. <br>
                <span class="font-bold">Technologies :</span> Vue.js 3, Tailwind CSS, JavaScript. <br>
                <span class="font-bold">Fonctionnalités clés :</span> Interface responsive et moderne, composants dynamiques, intégration d'effets visuels personnalisés et optimisation du SEO.
              </p>
            </div>
            <div class="flex items-center justify-between gap-4 mt-auto">
              <a href="https://github.com/judicaelkouly/MY_PORTFOLIO" class="inline-block">
                <button class="btn-github">
                  <Icon icon="ri:github-fill" width="16" />
                  <span>Github</span>
                </button>
              </a>
              <a href="https://my-portfolio-tan-five-64.vercel.app/" class="inline-block">
                <button class="btn-github">
                  <Icon icon="solar:link-outline" width="16" />
                  <span>Visiter</span>
                </button>
              </a>
            </div>
          </div>
        </div>


      </section>
    </main>

    <FooterView/>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue'
import FooterView from './FooterView.vue';
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400&display=swap');

:root {
  --cyan: #00e5ff;
  --cyan-dim: rgba(0, 229, 255, 0.15);
  --cyan-glow: 0 0 18px rgba(0, 229, 255, 0.4);
  --bg: #080d28;
  --bg2: #0d1436;
  --bg3: #111a42;
  --white: #ffffff;
  --muted: rgba(255, 255, 255, 0.6);
}

.tech-icons {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin-bottom: 1.25rem;
}

.tech-icon {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  border: 1.5px solid rgba(0, 229, 255, 0.15);
  background: var(--bg3);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: default;
  transition: all 0.3s ease;
}

.tech-icon:hover {
  border-color: var(--cyan);
  box-shadow: var(--cyan-glow);
  transform: translateY(-3px);
}

.btn-github {
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  border: none;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  border-radius: 100px;
  font-weight: 700;
  padding: 0.6rem 1.2rem;
  font-size: 0.8rem;
  line-height: 1rem;
  background-color: rgba(0, 0, 0, 0.4);
  box-shadow:
    inset 0 1px 0 0 rgba(255, 255, 255, 0.04),
    inset 0 0 0 1px rgba(255, 255, 255, 0.04);
  color: #fff;
}

.btn-github:hover {
  box-shadow:
    inset 0 1px 0 0 rgba(255, 255, 255, 0.08),
    inset 0 0 0 1px rgba(252, 232, 3, 0.08);
  color: #fce803;
  transform: translateY(-0.2rem);
  background-color: rgba(0, 0, 0, 0.6);
}
</style>
