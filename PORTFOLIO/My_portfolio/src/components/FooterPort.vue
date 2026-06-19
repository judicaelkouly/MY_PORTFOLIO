<template>
  <div class="overflow-hidden flex h-screen text-body">

    <!-- Sidebar -->
    <aside
  id="sidebar"
  :class="[
    'w-[300px] bg-surface border-r border-custom flex flex-col h-full absolute z-30 md:relative shadow-lg md:shadow-none rounded-xl [@media(max-width:479px)]:w-[300px]',
    sidebarOpen ? 'translate-x-0' : '-translate-x-full md:translate-x-0'
  ]"
  style="transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
>
  <!-- Logo -->
  <div class="header relative pb-4 border-b-2 border-r border-custom rounded-xl stars shrink-0 [@media(max-width:479px)]:w-[300px] ">
    <div class="max-w-7xl pt-4">
      <div
        class="profile-container mx-auto mb-2 bg-cover bg-center h-28 w-28 sm:h-36 sm:w-36 rounded-full"
        :style="{ backgroundImage: 'url(/myy.jpeg)' }"
      ></div>

      <h1 class="text-2xl font-semibold text-[#00e5ff] text-center">Judicael Kouly</h1>
      <div class="typewriter-line">
        <span class="text-green-900 text-center pl-10 mt-5">{{ typedText }}</span><span class="cursor"></span>
      </div>
    </div>
  </div>

  <!-- Navigation -->
  <div class="flex-1 overflow-y-auto py-6 px-4 flex flex-col gap-1">
    <a @click="switchTab('about')" :class="['nav-item', activeTab === 'about' ? 'active' : '']">
      <Icon icon="mdi:user-settings-variant" :ssr="true" width="24" />
      <span>À propos</span>
    </a>
    <a @click="switchTab('education')" :class="['nav-item', activeTab === 'education' ? 'active' : '']">
      <Icon icon="carbon:education" :ssr="true" width="24" />
      <span>Éducation</span>
    </a>
    <a @click="switchTab('capacites')" :class="['nav-item', activeTab === 'capacites' ? 'active' : '']">
      <Icon icon="lucide:cpu" :ssr="true" width="24" />

      <span>Capacités</span>
    </a>
    <a @click="switchTab('realisations')" :class="['nav-item', activeTab === 'realisations' ? 'active' : '']">
      <Icon icon="iconamoon:certificate-badge" :ssr="true" width="24" />
      <span>Réalisations</span>
    </a>
    <a @click="switchTab('contact')" :class="['nav-item', activeTab === 'contact' ? 'active' : '']">
      <Icon icon="mynaui:telephone" :ssr="true" width="24" />
      <span>Contact</span>
    </a>
  </div>

  <!-- User Profile -->
  <div class="p-5 border-t border-custom shrink-0 bg-[var(--bg)] m-4 rounded-xl">
    <div class="flex items-center gap-3">
      <div
        class="w-10 h-10 rounded-full flex items-center justify-center font-bold text-primary-custom border-2 border-surface shadow-sm"
        style="background-color: var(--primary-light);"
      >
        JK
      </div>
    </div>
  </div>
</aside>

    <!-- Overlay mobile -->
    <div
      v-if="sidebarOpen"
      class="fixed inset-0  bg-[var(--bg)] backdrop-blur-sm z-20 md:hidden"
      @click="toggleSidebar"
    ></div>

    <main class="flex-1 flex flex-col min-w-0 bg-[var(--bg)]">

  <header class="h-[80px] bg-surface border-b border-custom flex items-center justify-between px-6 shrink-0 z-10 sticky top-0 rounded-3xl">
    <div class="flex items-center gap-4">
      <button class="btn-icon md:!hidden text-[var(--text-main)]" @click="toggleSidebar">
        <Icon icon="hugeicons:menu-03" width="26" />
      </button>
    </div>

    <div class="flex items-center gap-3 sm:gap-5">
      <!-- Theme Toggle -->
      <button class="btn-icon bg-[var(--bg)] rounded-full hover:bg-[var(--border)]" @click="toggleTheme">
        <Icon :icon="isDark? 'solar:sun-bold-duotone' : 'solar:moon-bold-duotone'" width="22" :class="isDark? 'text-[#FFC107]' : 'text-[var(--text-main)]'" />
      </button>
    </div>
  </header>

  <!-- Un seul conteneur scrollable pour tout le contenu -->
  <div class="flex-1 overflow-y-auto p-5 sm:p-8" ref="scrollArea">
    <div class="max-w-[1400px] mx-auto">

      <!-- About content -->
       <div v-show="activeTab === 'about'" class="view-fade">
        <div class=" dark:bg-gray-800 ">
    <div class=" w-full mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 z-20">
        <h1 class="text-xl font-bold mb-4 text-center ">
                <span class="gradient-text">{{ typedWel }}</span><br>

            </h1>
        <h1 class="">
            <span class="text-xs ">Je suis </span> <br><span class="text-[#00e5ff] text-4xl md:text-6xl font-bold mb-4"> Judicael Kouly</span>
        </h1>
        <!-- <div class="lg:mt-0 lg:flex-shrink-0">
            <div class="mt-12 inline-flex rounded-md shadow m-5">
               <p class="text-xs font-medium mt-1"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-envelope-check" viewBox="0 0 16 16">
  <path d="M2 2a2 2 0 0 0-2 2v8.01A2 2 0 0 0 2 14h5.5a.5.5 0 0 0 0-1H2a1 1 0 0 1-.966-.741l5.64-3.471L8 9.583l7-4.2V8.5a.5.5 0 0 0 1 0V4a2 2 0 0 0-2-2zm3.708 6.208L1 11.105V5.383zM1 4.217V4a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v.217l-7 4.2z"/>
  <path d="M16 12.5a3.5 3.5 0 1 1-7 0 3.5 3.5 0 0 1 7 0m-1.993-1.679a.5.5 0 0 0-.686.172l-1.17 1.95-.547-.547a.5.5 0 0 0-.708.708l.774.773a.75.75 0 0 0 1.174-.144l1.335-2.226a.5.5 0 0 0-.172-.686"/>
</svg>judicaelkouluy@gmail.com</p>

            </div>
             <div class="mt-12 inline-flex rounded-md shadow ">
               <p class="text-xs font-medium mt-1 mr-5"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-geo-alt" viewBox="0 0 16 16">
  <path d="M12.166 8.94c-.524 1.062-1.234 2.12-1.96 3.07A32 32 0 0 1 8 14.58a32 32 0 0 1-2.206-2.57c-.726-.95-1.436-2.008-1.96-3.07C3.304 7.867 3 6.862 3 6a5 5 0 0 1 10 0c0 .862-.305 1.867-.834 2.94M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10"/>
  <path d="M8 8a2 2 0 1 1 0-4 2 2 0 0 1 0 4m0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6"/>
</svg>Abidjan, Côte D'Ivoire</p>
            </div>

        </div> -->

    </div>
</div>
        <AboutView />
       </div>


      <!-- Education content -->
      <div v-show="activeTab === 'education'" class="view-fade">
        <h1 class="font-bold text-[#00e5ff] text-4xl mb-6">Éducation</h1>
          <EducationView />
      </div>

      <!-- Capacites content -->
      <div v-show="activeTab === 'capacites'" class="view-fade">
        <CapaciteView />
      </div>

      <!-- Realisations content -->
      <div v-show="activeTab === 'realisations'" class="view-fade">
        <h1 class=" font-bold text-4xl mb-6">Mes Réalisations</h1>
        <RealisationView/>
      </div>

      <!-- Contact content -->
      <div v-show="activeTab === 'contact'" class="view-fade">
        <ContactView/>
      </div>

    </div>
  </div>
</main>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount, nextTick } from 'vue'
import { Icon } from '@iconify/vue'
import { Chart, registerables } from 'chart.js'
import EducationView from './EducationView.vue'
import AboutView from './AboutView.vue'
import CapaciteView from './CapaciteView.vue'
import ContactView from './ContactView.vue'
import RealisationView from './RealisationView.vue'

Chart.register(...registerables)

// ─── State ───────────────────────────────────────────────
const activeTab = ref('about')
const isDark = ref(false)
const sidebarOpen = ref(false)
const scrollArea = ref(null)
const chartTrenRef = ref(null)
const chartStatusRef = ref(null)

let chart1 = null
let chart2 = null

// ─── Typewriter (composable inline) ──────────────────────
function useTypewriter(phrases) {
  const text = ref('')
  let phraseIndex = 0, charIndex = 0, deleting = false, timer = null

  function type() {
    const current = phrases[phraseIndex]
    if (!deleting) {
      text.value = current.slice(0, ++charIndex)
      if (charIndex === current.length) {
        deleting = true
        timer = setTimeout(type, 2200)
        return
      }
    } else {
      text.value = current.slice(0, --charIndex)
      if (charIndex === 0) {
        deleting = false
        phraseIndex = (phraseIndex + 1) % phrases.length
      }
    }
    timer = setTimeout(type, deleting ? 28 : 52)
  }

  onMounted(() => type())
  onBeforeUnmount(() => clearTimeout(timer))
  return text
}

const typedText = useTypewriter(['Developpeur Web', 'Agent marketing'])
const typedWel  = useTypewriter(['Bienvenue sur mon portfolio', 'Bienvenue dans mon univers numérique'])

// ─── Theme ───────────────────────────────────────────────
function toggleTheme() {
  isDark.value = !isDark.value
  document.documentElement.classList.toggle('dark', isDark.value)
  localStorage.setItem('theme', isDark.value ? 'dark' : 'light')
  updateChartsTheme()
}

// ─── Sidebar ─────────────────────────────────────────────
function toggleSidebar() {
  sidebarOpen.value = !sidebarOpen.value
}

// ─── Navigation ──────────────────────────────────────────
function switchTab(tab) {
  activeTab.value = tab
  if (window.innerWidth < 768) sidebarOpen.value = false
  if (scrollArea.value) scrollArea.value.scrollTop = 0
  if (tab === 'about') {
    nextTick(() => {
      chart1?.resize()
      chart2?.resize()
    })
  }
}

// ─── Charts ──────────────────────────────────────────────
function initCharts() {
  if (!chartTrenRef.value || !chartStatusRef.value) return

  const dark        = isDark.value
  const primaryColor = dark ? '#634bea' : '#190182'
  const gridColor    = dark ? '#2A3645' : '#E9ECEF'
  const textColor    = dark ? '#94A3B8' : '#6C757D'
  const areaBgColor  = dark ? 'rgba(99,75,234,0.1)' : 'rgba(25,1,130,0.08)'
  const tooltipBg    = dark ? '#2A3645' : '#212529'

  chart1 = new Chart(chartTrenRef.value, {
    type: 'line',
    data: {
      labels: ['1 Mar', '5 Mar', '10 Mar', '15 Mar', '20 Mar', '25 Mar', '30 Mar'],
      datasets: [{
        label: 'Pendaftar Harian',
        data: [120, 190, 250, 210, 380, 420, 560],
        borderColor: primaryColor,
        backgroundColor: areaBgColor,
        borderWidth: 3,
        fill: true,
        tension: 0.4,
        pointBackgroundColor: dark ? '#1E1E1E' : '#FFFFFF',
        pointBorderColor: primaryColor,
        pointBorderWidth: 2,
        pointRadius: 4,
        pointHoverRadius: 6,
      }],
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      layout: { padding: { top: 10 } },
      plugins: {
        legend: { display: false },
        tooltip: {
          backgroundColor: tooltipBg,
          titleColor: '#FFF',
          bodyColor: '#FFF',
          padding: 12,
          cornerRadius: 8,
          displayColors: false,
          callbacks: { label: ctx => ctx.parsed.y + ' Pendaftar Baru' },
        },
      },
      scales: {
        y: {
          beginAtZero: true,
          grid: { color: gridColor, drawBorder: false, borderDash: [5, 5] },
          ticks: { color: textColor, font: { family: "'Plus Jakarta Sans', sans-serif", size: 11 }, padding: 10 },
        },
        x: {
          grid: { display: false },
          ticks: { color: textColor, font: { family: "'Plus Jakarta Sans', sans-serif", size: 11 }, padding: 10 },
        },
      },
    },
  })

  chart2 = new Chart(chartStatusRef.value, {
    type: 'doughnut',
    data: {
      labels: ['Diterima', 'Cadangan', 'Ditolak'],
      datasets: [{
        data: [320, 80, 120],
        backgroundColor: ['#28A745', '#6F42C1', '#DC3545'],
        borderWidth: 0,
        hoverOffset: 6,
      }],
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      cutout: '75%',
      plugins: {
        legend: { display: false },
        tooltip: {
          backgroundColor: tooltipBg,
          bodyFont: { family: "'Plus Jakarta Sans', sans-serif", size: 13 },
          padding: 12,
          cornerRadius: 8,
        },
      },
    },
  })
}

function updateChartsTheme() {
  chart1?.destroy()
  chart2?.destroy()
  chart1 = null
  chart2 = null
  nextTick(() => initCharts())
}

// ─── Lifecycle ───────────────────────────────────────────
onMounted(() => {
  const saved = localStorage.getItem('theme')
  if (saved === 'dark' || (!saved && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    isDark.value = true
    document.documentElement.classList.add('dark')
  }
  if (chartTrenRef.value || chartStatusRef.value) {
    initCharts()
  }
})

onBeforeUnmount(() => {
  chart1?.destroy()
  chart2?.destroy()
})
</script>


<style lang="scss">
/* ── CSS Variables ── */

@import 'https://fonts.googleapis.com/icon?family=Material+Icons';
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Playwrite+AU+VIC+Guides&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Sail&display=swap');




 @keyframes neon-pulse {
            0%, 100% { text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #00ffff, 0 0 35px #00ffff, 0 0 40px #00ffff, 0 0 50px #00ffff, 0 0 75px #00ffff; }
            50% { text-shadow: 0 0 2px #fff, 0 0 5px #fff, 0 0 7px #fff, 0 0 10px #00ffff, 0 0 17px #00ffff, 0 0 20px #00ffff, 0 0 25px #00ffff, 0 0 37px #00ffff; }
        }
        /* Test font */
        .playwrite-au-vic-guides-regular {
          font-family: "Playwrite AU VIC Guides", cursive;
          font-weight: 400;
          font-style: normal;
        }
        .sail-regular {
          font-family: "Sail", system-ui;
          font-weight: 400;
          font-style: normal;
        }
        .neon-text {
            animation: neon-pulse 1.5s infinite alternate;
        }

         .bg-animated {
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

         /* .cyber-grid {
            background-image: linear-gradient(rgba(0, 255, 255, 0.1) 1px, transparent 1px),
                              linear-gradient(90deg, rgba(0, 255, 255, 0.1) 1px, transparent 1px);
            background-size: 20px 20px;
            animation: cyber-grid-move 20s linear infinite;
        } */

        @keyframes cyber-grid-move {
            0% { background-position: 0 0; }
            100% { background-position: 20px 20px; }
        }

        .feature-card {
            backdrop-filter: blur(10px);
            background-color: rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(0, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
        }

        .feature-icon {
            transition: all 0.3s ease;
        }

        .feature-card:hover .feature-icon {
            transform: rotate(360deg) scale(1.2);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .floating {
            animation: float 6s ease-in-out infinite;
        }

        .glitch-effect {
            position: relative;
            overflow: hidden;
        }

        .glitch-effect::before,
        .glitch-effect::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }

        .glitch-effect::before {
            left: 2px;
            text-shadow: -2px 0 #ff00de;
            clip: rect(24px, 550px, 90px, 0);
            animation: glitch-anim 3s infinite linear alternate-reverse;
        }

        .glitch-effect::after {
            left: -2px;
            text-shadow: -2px 0 #00ffff;
            clip: rect(85px, 550px, 140px, 0);
            animation: glitch-anim 2s infinite linear alternate-reverse;
        }

        @keyframes glitch-anim {
            0% { clip: rect(39px, 9999px, 71px, 0); }
            20% { clip: rect(3px, 9999px, 5px, 0); }
            40% { clip: rect(6px, 9999px, 38px, 0); }
            60% { clip: rect(13px, 9999px, 43px, 0); }
            80% { clip: rect(44px, 9999px, 93px, 0); }
            100% { clip: rect(54px, 9999px, 47px, 0); }
        }
/* //////////////////////////////////// */



@keyframes move-background {
  from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}
@-webkit-keyframes move-background {
  from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}

@-moz-keyframes move-background {
	from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}

    @-webkit-keyframes move-background {
	from {
		-webkit-transform: translate3d(0px, 0px, 0px);
	}
	to {
		-webkit-transform: translate3d(1000px, 0px, 0px);
	}
}



.stars {
 background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/1231630/stars.png) repeat;

}

.hr-text {
  line-height: 1em;
  position: relative;
  outline: 0;
  border: 0;
  color: black;
  text-align: center;
  height: 1.5em;
  opacity: 0.5;
}
.hr-text:before {
  content: "";
  background: linear-gradient(to right, transparent, #818078, transparent);
  position: absolute;
  left: 0;
  top: 50%;
  width: 100%;
  height: 1px;
}
.hr-text:after {
  content: attr(data-content);
  position: relative;
  display: inline-block;
  color: black;
  padding: 0 0.5em;
  line-height: 1.5em;
  color: #818078;
  background-color: #fcfcfa;
}


 /* HERO */
  .hero {
    padding: 7rem 2rem 5rem;
    max-width: 900px;
    margin: 0 auto;
  }

  .hero-eyebrow {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 24px;
    height: 1px;
    background: var(--accent);
  }

  .hero-title {
    font-family: var(--font-display);
    font-size: clamp(2.4rem, 5vw, 3.8rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 1.5rem;
  }

  .hero-title .name { display: block; color: var(--text); }
  .hero-title .role { display: block; color: var(--muted); font-weight: 400; }

  .typewriter-line {
    font-family: var(--font-mono);
    font-size: clamp(1rem, 2.5vw, 1.4rem);
    color: var(--accent);
    display: flex;
    align-items: center;
    gap: 2px;
    margin-bottom: 2rem;
    min-height: 2rem;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1.2em;
    background: var(--accent);
    animation: blink 1s step-end infinite;
    vertical-align: middle;
  }

  @keyframes blink { 50% { opacity: 0; } }

  .hero-desc {
    color: var(--muted);
    font-size: 15px;
    max-width: 540px;
    line-height: 1.8;
    margin-bottom: 2.5rem;
  }

  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn-primary {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.04em;
    padding: 10px 24px;
    background: var(--accent);
    color: #0A0A0F;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.2s, transform 0.15s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-primary:hover { background: #6FFFD4; transform: translateY(-1px); }

  .btn-secondary {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.04em;
    padding: 10px 24px;
    background: transparent;
    color: var(--text);
    border: 1px solid var(--border);
    border-radius: 4px;
    cursor: pointer;
    transition: border-color 0.2s, transform 0.15s;
    text-decoration: none;
    display: inline-block;
  }

  .btn-secondary:hover { border-color: rgba(255,255,255,0.25); transform: translateY(-1px); }

:root {
  --cyan:#00e5ff;
  --primary: #190182;
  --primary-dark: #12015c;
  --primary-light: rgba(25, 1, 130, 0.08);
  --bg: #080d28;
  --surface: #FFFFFF;
  --text-main: #FFFFFF;
  --text-secondary: #FFFFFF;
  --text-tertiary: #FFFFFF;
  --border: rgba(0,229,255,0.18);
  --border-light: #F1F3F5;
  --success: #28A745;
  --success-light: rgba(40, 167, 69, 0.12);
  --danger: #DC3545;
  --danger-light: rgba(220, 53, 69, 0.12);
  --warning: #FFC107;
  --warning-dark: #D39E00;
  --warning-light: rgba(255, 193, 7, 0.15);
  --info: #17A2B8;
  --info-light: rgba(23, 162, 184, 0.12);
  --purple: #6F42C1;
  --purple-light: rgba(111, 66, 193, 0.12);
  --shadow-sm: 0 2px 4px rgba(25,1,130,0.02), 0 4px 12px rgba(25,1,130,0.04);
  --shadow-md: 0 4px 12px rgba(25,1,130,0.05), 0 12px 24px rgba(25,1,130,0.08);
}
.dark {
  --primary: #634bea;
  --primary-dark: #190182;
  --primary-light: rgba(99, 75, 234, 0.15);
  --bg: #121212;
  --surface: #1E1E1E;
  --text-main: #F8FAFC;
  --text-secondary: #CBD5E1;
  --text-tertiary: #94A3B8;
  --border: #334155;
  --border-light: #2A3645;
  --warning-dark: #FFC107;
  --shadow-sm: 0 4px 6px -1px rgba(0,0,0,0.4);
  --shadow-md: 0 10px 20px -5px rgba(0,0,0,0.5);
}

body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background-color: var(--bg);
  color: var(--text-secondary);
  transition: background-color 0.3s, color 0.3s;
}
.font-mono { font-family: 'JetBrains Mono', monospace; }

/*h1 { font-size: 1.875rem; font-weight: 700; color: var(--text-main); letter-spacing: -0.02em; }*/
/*h2 { font-size: 1.5rem; font-weight: 700; color: var(--primary); letter-spacing: -0.01em; }*/
h3 { font-size: 1.25rem; font-weight: 700; color: var(--cyan); }
h4 { font-size: 1.125rem; font-weight: 600; color: var(--text-main); }
.text-body { font-size: 0.9375rem; font-weight: 400; color: var(--text-secondary); line-height: 1.6; }
.text-caption { font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em; color: var(--text-tertiary); }
.text-data { font-size: 1.5rem; font-weight: 700; color: var(--text-main); font-family: 'JetBrains Mono', monospace; line-height: 1.2; }

.card-panel {
  background-color: var(--surface);
  border-radius: 16px;
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--border-light);
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}
.card-panel:hover { box-shadow: var(--shadow-md); }

.stat-card {
  background-color: var(--surface);
  border-left: 4px solid var(--primary);
  border-right: 1px solid var(--border-light);
  border-top: 1px solid var(--border-light);
  border-bottom: 1px solid var(--border-light);
  border-radius: 12px;
  padding: 16px 20px;
  box-shadow: var(--shadow-sm);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 110px;
  transition: transform 0.2s;
}
.stat-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-md); }

.btn-primary {
  background-color: var(--primary);
  color: #FFF;
  padding: 8px 18px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.875rem;
  transition: all 0.2s;
  border: none;
  cursor: pointer;
  display: inline-flex; align-items: center; justify-content: center; gap: 8px;
}
.btn-primary:hover { background-color: var(--primary-dark); transform: translateY(-1px); }

.btn-outline {
  border: 1px solid var(--border);
  color: var(--text-main);
  background: var(--surface);
  padding: 8px 18px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.875rem;
  transition: all 0.2s;
  cursor: pointer;
  display: inline-flex; align-items: center; justify-content: center; gap: 8px;
}
.btn-outline:hover { background-color: var(--bg); border-color: var(--text-tertiary); }

.btn-icon {
  width: 36px; height: 36px;
  border-radius: 8px;
  display: inline-flex; justify-content: center; align-items: center;
  transition: all 0.2s;
  color: var(--text-tertiary);
  background: transparent;
  border: none;
  cursor: pointer;
}
.btn-icon:hover { background-color: var(--primary-light); color: var(--primary); }

.badge {
  padding: 4px 10px;
  border-radius: 6px;
  font-size: 0.75rem;
  font-weight: 600;
  display: inline-flex; align-items: center; gap: 6px;
  letter-spacing: 0.02em;
}
.badge-success { background-color: var(--success-light); color: var(--success); }
.badge-warning { background-color: var(--warning-light); color: var(--warning-dark); }
.badge-danger  { background-color: var(--danger-light);  color: var(--danger); }
.badge-info    { background-color: var(--info-light);    color: var(--info); }
.badge-purple  { background-color: var(--purple-light);  color: var(--purple); }

.input-solid {
  background-color: var(--bg);
  border: 1px solid var(--border);
  color: var(--text-main);
  border-radius: 8px;
  padding: 10px 16px;
  width: 100%;
  font-size: 0.875rem;
  font-weight: 500;
  transition: all 0.2s;
  font-family: inherit;
}
.input-solid:focus {
  outline: none;
  border-color: var(--primary);
  background-color: var(--surface);
  box-shadow: 0 0 0 3px var(--primary-light);
}

.table-custom { width: 100%; border-collapse: separate; border-spacing: 0; }
.table-custom th {
  background-color: var(--bg);
  color: var(--text-tertiary);
  font-weight: 600;
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 14px 20px;
  text-align: left;
  border-bottom: 1px solid var(--border);
}
.table-custom td {
  padding: 16px 20px;
  border-bottom: 1px solid var(--border-light);
  color: var(--text-secondary);
  font-size: 0.875rem;
  vertical-align: middle;
  transition: background-color 0.2s;
}
.table-custom tbody tr:hover td { background-color: var(--primary-light); }
.table-custom tbody tr:last-child td { border-bottom: none; }

.nav-item {
  display: flex; align-items: center; gap: 14px;
  padding: 12px 18px;
  color: var(--text-secondary);
  border-radius: 10px;
  margin-bottom: 4px;
  font-weight: 600;
  font-size: 0.9375rem;
  transition: all 0.2s;
  cursor: pointer;
  text-decoration: none;
}
.nav-item:hover { background-color: var(--primary-light); color: var(--primary); }
.nav-item.active { background-color: var(--primary); color: #FFF; box-shadow: 0 4px 12px var(--primary-light); }

.timeline-item { position: relative; padding-left: 28px; padding-bottom: 20px; }
.timeline-item::before {
  content: ''; position: absolute; left: 7px; top: 4px; bottom: 0;
  width: 2px; background-color: var(--border);
}
.timeline-item:last-child::before { display: none; }
.timeline-dot {
  position: absolute; left: 0; top: 4px;
  width: 16px; height: 16px;
  border-radius: 50%;
  background-color: var(--primary);
  border: 3px solid var(--surface);
  z-index: 1;
}


.text-primary-custom { color: var(--primary); }
.border-custom { border-color: var(--border); }

/* View fade animation */
.view-fade { animation: fadeIn 0.35s cubic-bezier(0.4, 0, 0.2, 1) forwards; }
@keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--text-tertiary); border-radius: 10px; }
::-webkit-scrollbar-thumb:hover { background: var(--primary); }
</style>
