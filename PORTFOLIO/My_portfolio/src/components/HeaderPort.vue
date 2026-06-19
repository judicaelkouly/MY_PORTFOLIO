<template>
  <body class="bg-gray-900">
  <header class="flex items-center justify-between px-6 py-3 md:py-4 shadow max-w-5xl rounded-full mx-auto w-full relative">

    <a href="">
      <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" fill="currentColor" color="blue" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M1.114 8.063V7.9c1.005-.102 1.497-.615 1.497-1.6V4.503c0-1.094.39-1.538 1.354-1.538h.273V2h-.376C2.25 2 1.49 2.759 1.49 4.352v1.524c0 1.094-.376 1.456-1.49 1.456v1.299c1.114 0 1.49.362 1.49 1.456v1.524c0 1.593.759 2.352 2.372 2.352h.376v-.964h-.273c-.964 0-1.354-.444-1.354-1.538V9.663c0-.984-.492-1.497-1.497-1.6M14.886 7.9v.164c-1.005.103-1.497.616-1.497 1.6v1.798c0 1.094-.39 1.538-1.354 1.538h-.273v.964h.376c1.613 0 2.372-.759 2.372-2.352v-1.524c0-1.094.376-1.456 1.49-1.456v-1.3c-1.114 0-1.49-.362-1.49-1.456V4.352C14.51 2.759 13.75 2 12.138 2h-.376v.964h.273c.964 0 1.354.444 1.354 1.538V6.3c0 .984.492 1.497 1.497 1.6M7.5 11.5V9.207l-1.621 1.621-.707-.707L6.792 8.5H4.5v-1h2.293L5.172 5.879l.707-.707L7.5 6.792V4.5h1v2.293l1.621-1.621.707.707L9.208 7.5H11.5v1H9.207l1.621 1.621-.707.707L8.5 9.208V11.5z"/>
      </svg>
    </a>

    <!-- Desktop nav -->
    <nav class="hidden md:block">
      <ul class="flex space-x-8 text-sm font-medium">
        <li><a href="#" class="hover:text-indigo-600 transition-colors">Home</a></li>
        <li><a href="#" class="hover:text-indigo-600 transition-colors">About</a></li>
        <li><a href="#" class="hover:text-indigo-600 transition-colors">Éducation</a></li>
        <li><a href="#" class="hover:text-indigo-600 transition-colors">Réalisations</a></li>

      </ul>
    </nav>

    <div class="flex items-center space-x-4">
      <!-- Theme toggle -->
      <button class="size-8 flex items-center justify-center hover:bg-gray-100 transition border border-slate-300 rounded-md">
        <svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M7.5 10.39a2.889 2.889 0 1 0 0-5.779 2.889 2.889 0 0 0 0 5.778M7.5 1v.722m0 11.556V14M1 7.5h.722m11.556 0h.723m-1.904-4.596-.511.51m-8.172 8.171-.51.511m-.001-9.192.51.51m8.173 8.171.51.511" stroke="#353535" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>

              <a class="hidden md:flex bg-indigo-600 text-white px-5 py-2 rounded-full text-sm font-medium hover:bg-indigo-700 transition" href="#">
            Contact
        </a>

      <!-- Hamburger -->
      <button class="md:hidden text-gray-600" @click="mobileMenuOpen = true" aria-label="Open menu">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </div>

    <!-- Mobile menu overlay -->
    <Transition
      enter-active-class="transition ease-out duration-200"
      enter-from-class="opacity-0 -translate-y-2"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition ease-in duration-150"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-2"
    >
      <div v-if="mobileMenuOpen" class="md:hidden absolute top-0 left-0 w-full bg-white rounded-3xl shadow-lg px-6 py-4 z-50">
        <div class="flex items-center justify-between mb-4">
          <span class="font-semibold text-gray-800">Menu</span>
          <button @click="mobileMenuOpen = false" class="text-gray-500 hover:text-gray-800" aria-label="Close menu">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
              <path d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>

        <ul class="flex flex-col gap-3 text-sm font-medium text-gray-700">
          <li><a href="#" @click="mobileMenuOpen = false" class="block hover:text-indigo-600">Home</a></li>
          <li><a href="#" @click="mobileMenuOpen = false" class="block hover:text-indigo-600">About</a></li>
          <li><a href="#" @click="mobileMenuOpen = false" class="block hover:text-indigo-600">Projets</a></li>
          <li><a href="#" @click="mobileMenuOpen = false" class="block hover:text-indigo-600">Curriculum</a></li>
          <li>
            <a href="#" class="block bg-indigo-600 text-white text-center px-4 py-2 rounded-full hover:bg-indigo-700 transition">
              Contactez-moi
            </a>
          </li>
        </ul>
      </div>
    </Transition>

  </header>


  <div>
  <div class="flex h-screen items-center justify-center bg-gray-900 p-5">
    <div class="grid md:grid-cols-2 grid-cols-1 items-center gap-10 md:px-10">
      <div>
        <h1 class="mb-2 text-3xl text-center font-bold text-white">A propos de moi</h1> <br>
        <h1 class="mb-2 text-3xl font-bold text-white"><span class="text-green-500">Judicael,</span> Je suis developpeur full stack</h1>
        <p class="mb-6 text-white">
Bienvenue dans mon univers numérique. <br>
Je crois que le digital peut transformer la manière dont nous créons, communiquons et entreprenons.
À travers ce portfolio, je te présente mon parcours et ma contribution à cet univers en constante évolution.        </p>

      </div>
      <div>
        <img src="../../public/profile.png" alt="" class="md:size-96 size-72 rounded-full ml-9" />
      </div>
    </div>
  </div>
</div>

<div class="bg-gray-900">
<h1 class="text-3xl font-semibold text-white text-center mx-auto">Mes Projets </h1>
<p class="text-sm text-slate-500 text-center mt-2 max-w-lg mx-auto">
    Stay ahead of the curve with fresh content on code, design, startups, and everything in between.
</p>

<div class="flex flex-wrap items-center justify-center gap-8 pt-12 ">
    <div class="max-w-72 w-full hover:-translate-y-0.5 transition duration-300">
        <img class="rounded-xl" src="https://images.unsplash.com/photo-1590650516494-0c8e4a4dd67e?w=1200&h=800&auto=format&fit=crop&q=60" alt="">
        <h3 class="text-base text-white font-medium mt-3">Color Psychology in UI: How to Choose the Right Palette</h3>
        <p class="text-xs text-indigo-600 font-medium mt-1">UI/UX design</p>
    </div>
    <div class="max-w-72 w-full hover:-translate-y-0.5 transition duration-300">
        <img class="rounded-xl" src="https://images.unsplash.com/photo-1714974528646-ea024a3db7a7?w=1200&h=800&auto=format&fit=crop&q=60" alt="">
        <h3 class="text-base text-white font-medium mt-3">Color Psychology in UI: How to Choose the Right Palette</h3>
        <p class="text-xs text-indigo-600 font-medium mt-1">UI/UX design</p>
    </div>
    <div class="max-w-72 w-full hover:-translate-y-0.5 transition duration-300">
        <img class="rounded-xl" src="https://images.unsplash.com/photo-1713947501966-34897f21162e?w=1200&h=800&auto=format&fit=crop&q=60" alt="">
        <h3 class="text-base text-white font-medium mt-3">Color Psychology in UI: How to Choose the Right Palette</h3>
        <p class="text-xs text-indigo-600 font-medium mt-1">UI/UX design</p>
    </div>
</div>
</div>


<div class="bg-gray-900">
<h1 class="text-3xl font-semibold text-white text-center mx-auto pt-12">Technologies skills </h1>

<div class="flex flex-wrap items-center justify-center  gap-8 pt-12 ">

<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">HTML5/CSS </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">Javascript </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">React </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">Next Js </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">Nest Js </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">Vue Js </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">Taiwind css </a></button><!----></div></div></div>
<div class="flex flex-col items-center justify-center gap-4 sm:gap-2" data-animate="" style="--stagger: 4;"><div class="flex flex-col items-center justify-center gap-4 sm:flex-row sm:gap-2"><div class="relative inline-flex"><button class="group relative inline-flex items-center overflow-hidden transition rounded-md px-8 py-1 bg-green-800"><div class="absolute inset-0 flex items-center [container-type:inline-size]"><div class="absolute size-[100cqw] animate-spin bg-[conic-gradient(from_0_at_50%_50%,rgba(255,255,255,0.5)_0deg,transparent_60deg,transparent_300deg,rgba(255,255,255,0.5)_360deg)] opacity-0 transition duration-300 group-hover:opacity-100"></div></div><div class="absolute inset-0.5 bg-green-900 sm:bg-green-900/80 sm:backdrop-blur-md bg-zinc-800 rounded-md"></div><div class="absolute bottom-0 left-1/2 h-1/3 w-4/5 -translate-x-1/2 bg-white/10 opacity-50 blur-md transition-all duration-500 group-hover:h-2/3 group-hover:opacity-100 rounded-md"></div><a href="/contact" class="white-gradient relative flex items-center justify-center gap-2 transition-all duration-200 text-white">TypeScript </a></button><!----></div></div></div>

</div>
</div>


<div class="container pt-5">
	<div class="blob-c">
	<div class="shape-blob"></div>
	<div class="shape-blob one"></div>
	<div class="shape-blob two"></div>
	<div class="shape-blob three"></div>
    <div class="shape-blob four"></div>
    <div class="shape-blob five"></div>
    <div class="shape-blob six"></div>
	</div>
        <h1 class="mb-2 text-3xl text-center font-bold text-white">{Fin}</h1> <br>
</div>


  </body>


</template>

<script setup lang="ts">
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

</script>


<style>


@import url('https://fonts.googleapis.com/css?family=Playfair+Display:400,900');

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');


@import url('https://pro.fontawesome.com/releases/v6.0.0-beta1/css/all.css');

button.neumorphic {
  container-type: inline-size;
  aspect-ratio: 1/1;
  border: 0.5rem solid transparent;
  border-radius: 1rem;
  color: hsl(0 0% 10%);
  background: none;

  display: grid;
  place-content: center;
  gap: 1rem;

  --shadow:
    -.5rem -.5rem 1rem hsl(0 0% 100% / .75),
    .5rem .5rem 1rem hsl(0 0% 50% / .5);
  box-shadow: var(--shadow);
  outline: none;
  transition: all 0.1s;

  &:hover, &:focus-visible {
    color: hsl(10 80% 50%);
    scale: 1.1
  }
  &:active, &.active{
    box-shadow:
      var(--shadow),
      inset .5rem .5rem 1rem hsl(0 0% 50% / .5),
      inset -.5rem -.5rem 1rem hsl(0 0% 100% / .75);
    color: hsl(10 80% 50%);
    > i { font-size: 28cqi};
    > span { font-size: 13cqi};
  }

  >i {
    font-size: 31cqi;
  }
  > span {
    font-family: system-ui, sans-serif;
    font-size: 16cqi;
  }
}

.buttons {
  display: grid;
  width: min(75rem, 100%);
  margin-inline: auto;
  grid-template-columns: repeat(auto-fit, minmax(min(8rem, 100%), 1fr));
  gap: 2rem;
}

    * {
        font-family: 'Poppins', sans-serif;
    }
body {
	margin: 0;
	padding: 0;
}

.container {
	background:#1F2024;
	min-height: 100vh;
	display: flex;
	flex-direction: row;
	align-items: center;
	justify-content: center;
	overflow: hidden;
	position: relative;
}

.blob-c {
	min-height: 100vh;
	overflow: hidden;
	position:absolute;
	width: 100%;
	filter: blur(40px);
/*   background: rgba(255,255,255,0.1) */
}

.shape-blob {
	background:#26C3F9;
	height: 60px;
	width: 80px;
	border-radius: 40% 50% 30% 40%;
  	animation:
		transform 18s ease-in-out infinite both alternate,
		movement_one 12s ease-in-out infinite both;
	opacity:.7;
	position: absolute;
	left: 75%;
	top: 40%;
}
.shape-blob.one{
	background:#0085FF;
	height: 150px;
	width: 200px;
	left: 10px;
	top: 10px;
	transform: rotate(-180deg);
	animation: transform 8s ease-in-out infinite both alternate, movement_two 20s ease-in-out infinite both;
}

.shape-blob.six{
	background:#0EAFFF;
	height: 70px;
	width: 100px;
	left: 160px;
	top: 200px;
	transform: rotate(-180deg);
	animation: transform 5s ease-in-out infinite both alternate, movement_two 5s ease-in-out infinite both;
}

.shape-blob.four{
	background:#4EAEFF;
	height: 100px;
	width: 80px;
	left: 350px;
	top: 60px;
	transform: rotate(-180deg);
	animation: transform 17s ease-in-out infinite both alternate, movement_two 13s ease-in-out infinite both;
}

.shape-blob.five{
	background:#0085FF;
	height: 100px;
	width: 80px;
	left: 480px;
	top: 30px;
	transform: rotate(-180deg);
	animation: transform 12s ease-in-out infinite both alternate, movement_two 18s ease-in-out infinite both;
}

.shape-blob.two{
	background:#4EAEFF;
	height: 150px;
	width: 150px;
	left: 600px;
	top: 150px;
	transform: rotate(-180deg);
	animation: transform 10s ease-in-out infinite both alternate, movement_two 10s ease-in-out infinite both;
}

.shape-blob.three{
	background:#0EAFFF;
	height: 150px;
	width: 150px;
	left: 800px;
	top: 30px;
	transform: rotate(-180deg);
	animation: transform 7s ease-in-out infinite both alternate, movement_two 23s ease-in-out infinite both;
}

@keyframes transform
{
    0%,
  100% { border-radius: 33% 67% 70% 30% / 30% 40% 70% 70%; }
   20% { border-radius: 37% 63% 51% 49% / 37% 35% 35% 63%; }
   40% { border-radius: 36% 64% 64% 36% / 64% 48% 52% 26%; }
   60% { border-radius: 37% 63% 51% 49% / 30% 30% 70% 73%; }
   80% { border-radius: 40% 60% 42% 58% / 51% 51% 49% 59%; }
}


@keyframes movement_one
{
    0%,
  100% { transform: none; }
   50% { transform: translate(50%, 20%) rotateY(10deg) scale(1); }
}

@keyframes movement_two
{
    0%,
  500% { transform: none; }
   50% { transform: translate(50%, 20%) rotate(-200deg) scale(1.3);}
}

/* h1 {
	font-family: 'Playfair Display', serif;
	font-size: 5em;
	letter-spacing: 2px;
	font-weight: 900;
	color: white;
	line-height: .9em;
	position: absolute;
	z-index: 4;
	text-shadow: 2px 3px 15px rgba(0,0,0,.15);
} */

*:before,
*:after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 16px;
  scroll-behavior: smooth;
}

@media (min-width: 768px) {
  html {
    font-size: 18px;
  }
}

@media (min-width: 1200px) {
  html {
    font-size: 20px;
  }
}

body {
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--text-primary);
  background-color: var(--background-dark);
  font-family: var(--font-secondary);
  font-size: var(--font-size-small);
}

.section {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.hero-section {
  padding: var(--spacing-large);
}

.fin-section {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--background-dark);
  z-index: 20;
  position: relative;
}

.fin-text {
  font-family: var(--font-primary);
  font-size: 3rem;
  color: var(--text-secondary);
  text-transform: none;
  letter-spacing: 0.05em;
}

body::after {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background-image: url("https://img.freepik.com/premium-photo/white-dust-scratches-black-background_279525-2.jpg?w=640"); */
  background-repeat: repeat;
  opacity: 0.2;
  mix-blend-mode: multiply;
  pointer-events: none;
  z-index: 1;
  filter: invert(0);
}

#container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: #0f0f0f;
  z-index: 0;
  pointer-events: none;
}

#ui-container {
  position: fixed;
  top: 10px;
  right: 10px;
  z-index: 100;
  opacity: 0.8;
  transition: opacity var(--transition-fast);
}

#ui-container:hover {
  opacity: 1;
}

#stats {
  position: fixed;
  top: 10px;
  left: 10px;
  z-index: 100;
}

.header-area {
  position: fixed;
  top: var(--spacing-large);
  left: 0;
  width: 100%;
  padding: 0 var(--spacing-large);
  display: flex;
  justify-content: center;
  z-index: 10;
}

.logo-container {
  position: absolute;
  left: var(--spacing-large);
  top: 0;
  display: flex;
  align-items: center;
  height: 2rem;
  z-index: 10;
  cursor: pointer;
}

.logo-circles {
  position: relative;
  width: 100%;
  height: 100%;
}

.circle {
  position: absolute;
  border-radius: 50%;
  transition: transform var(--transition-medium);
  width: 1.4rem;
  height: 1.4rem;
  background-color: var(--text-primary);
  top: 50%;
}

.circle-1 {
  left: 0;
  transform: translate(0, -50%);
}

.circle-2 {
  left: 0.8rem;
  transform: translate(0, -50%);
  mix-blend-mode: exclusion;
}

.logo-container:hover .circle-1 {
  transform: translate(-0.5rem, -50%);
}

.logo-container:hover .circle-2 {
  transform: translate(0.5rem, -50%);
}

.center-logo {
  text-align: center;
  z-index: 10;
  height: 2rem;
}

#logo-text {
  font-family: var(--font-primary);
  font-weight: 400;
  font-size: var(--font-size-medium);
  line-height: 1;
  margin: 0;
  color: var(--text-primary);
  text-transform: none;
}

.hero {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  z-index: 10;
  color: var(--text-primary);
  width: 90%;
  max-width: 800px;
}

.hero h1 {
  font-family: var(--font-primary);
  font-weight: 400;
  font-size: var(--font-size-large);
  line-height: 0.9;
  letter-spacing: -0.02em;
  color: var(--text-primary);
  text-transform: none;
  margin-bottom: 2rem;
  margin: 0 0 2rem 0;
}

.hero h2 {
  font-family: var(--font-secondary);
  font-size: var(--font-size-small);
  color: var(--text-secondary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  line-height: 1.4;
  opacity: 0.7;
  transition: opacity var(--transition-fast);
  font-weight: normal;
  margin: 0;
}

.hero:hover h2 {
  opacity: 1;
}

.contact-info {
  position: fixed;
  top: 50%;
  left: var(--spacing-large);
  transform: translateY(-50%);
  z-index: 10;
  font-family: var(--font-secondary);
  letter-spacing: 0.05em;
  font-size: var(--font-size-small);
  color: var(--text-primary);
  text-transform: uppercase;
}

.contact-heading {
  font-size: var(--font-size-small);
  color: var(--text-secondary);
  margin-bottom: var(--spacing-small);
}

.contact-email {
  display: block;
  color: var(--text-primary);
  text-decoration: none;
  transition: all var(--transition-fast);
  cursor: pointer;
}

.contact-email:hover {
  color: var(--text-secondary);
}

.footer-links {
  position: fixed;
  bottom: var(--spacing-large);
  left: var(--spacing-large);
  z-index: 10;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.25rem;
  font-family: var(--font-sans);
  font-weight: 400;
  font-size: var(--font-size-regular);
}

.footer-link {
  color: var(--text-secondary);
  text-decoration: none;
  transition: all var(--transition-fast);
  position: relative;
  padding-left: 0;
  text-transform: none;
  font-size: 1rem;
}

.footer-link::before {
  content: "";
  position: absolute;
  left: 0;
  top: 50%;
  width: 0;
  height: 1px;
  background-color: var(--text-primary);
  transform: translateY(-50%);
  transition: width var(--transition-fast), opacity var(--transition-fast);
  opacity: 0;
}

.footer-link:hover {
  color: var(--text-primary);
  padding-left: 1.2rem;
}

.footer-link:hover::before {
  width: 0.8rem;
  opacity: 1;
}

.coordinates {
  position: fixed;
  bottom: var(--spacing-large);
  right: var(--spacing-large);
  text-align: right;
  z-index: 10;
  font-family: var(--font-secondary);
  font-size: var(--font-size-small);
  color: var(--text-secondary);
}

.tp-dfwv {
  min-width: 280px !important;
}

.section {
  transition: all 0.6s ease;
}

@media (max-width: 768px) {
  .hero h1 {
    font-size: 3rem;
  }

  .footer-links {
    gap: 0.4rem;
  }

  .coordinates {
    font-size: 10px;
  }

  .hero p {
    font-size: 10px;
  }

  .story-display {
    width: 90%;
    font-size: 0.8rem;
  }
}

@media (max-width: 480px) {
  .hero-section {
    padding: var(--spacing-medium);
  }

  .header-area,
  .contact-info,
  .footer-links,
  .coordinates {
    padding: 0 var(--spacing-medium);
  }

  .logo-container,
  .contact-info,
  .footer-links {
    left: var(--spacing-medium);
  }

  .coordinates {
    right: var(--spacing-medium);
  }

  .hero h1 {
    font-size: 2.2rem;
  }

  .circle {
    width: 1.2rem;
    height: 1.2rem;
  }

  .circle-2 {
    left: 0.7rem;
  }

  #logo-text {
    font-size: 1.3rem;
  }

  .contact-heading {
    font-size: 10px;
  }

  .contact-email {
    font-size: 10px;
  }

  .story-display {
    width: 95%;
    font-size: 0.75rem;
  }
}

</style>
