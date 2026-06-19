<template>
  <div class="flex h-screen w-full relative">
    <!-- OVERLAY MOBILE -->
    <div
      v-show="isSidebarOpen"
      @click="toggleSidebar"
      class="fixed inset-0 bg-black/50 z-20 lg:hidden backdrop-blur-sm transition-all duration-300"
      :class="{ 'opacity-100': isSidebarOpen, 'opacity-0':!isSidebarOpen }"
    ></div>

    <!-- SIDEBAR -->
     <aside
      id="sidebar"
      class="fixed lg:relative z-30 w-72 h-full bg-white dark:bg-dark-card flex flex-col justify-between border-r border-gray-100 dark:border-gray-800 transition-transform duration-300 shadow-xl lg:shadow-none"
      :class="sidebarClasses"
    >
      <div class="p-8 flex items-center gap-3">
        <div class="w-10 h-10 rounded-xl bg-primary-500 flex items-center justify-center text-white shadow-glow">
          <i class="ph-bold ph-squares-four text-xl"></i>
        </div>
        <h1 class="text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Taskify<span class="text-primary-500">.</span></h1>
      </div>

      <!-- Navigation Links -->
      <nav class="flex-1 px-4 space-y-2 overflow-y-auto">
        <p class="px-4 text-xs font-semibold text-gray-400 uppercase tracking-wider mb-2 mt-4">Menu Utama</p>

        <a
          v-for="item in menuItems"
          :key="item.id"
          href="#"
          @click.prevent="switchPage(item.id)"
          class="nav-item flex items-center gap-3 px-4 py-3.5 rounded-2xl font-medium transition-all duration-300"
          :class="currentPage === item.id? activeClasses : inactiveClasses"
        >
          <i :class="item.icon + ' text-xl'"></i>
          {{ item.label }}
          <span v-if="item.badge" class="ml-auto bg-primary-100 text-primary-700 dark:bg-primary-900 dark:text-primary-300 text-[10px] px-2 py-0.5 rounded-full font-bold">{{ item.badge }}</span>
        </a>
      </nav>

      <div class="p-6 border-t border-gray-100 dark:border-gray-800">
        <div class="flex items-center gap-4 bg-gray-50 dark:bg-gray-800 p-3 rounded-2xl border border-gray-100 dark:border-gray-700">
          <img src="https://ui-avatars.com/api/?name=Dimas+Rizky&background=4900c7&color=fff" alt="User" class="w-10 h-10 rounded-full border-2 border-white dark:border-gray-600 shadow-sm">
          <div class="flex-1 min-w-0">
            <p class="text-sm font-bold text-gray-900 dark:text-white truncate">Dimas Rizky</p>
            <p class="text-xs text-gray-400 truncate">Pro Member</p>
          </div>
          <button @click="logout" class="text-gray-400 hover:text-red-500 transition-all duration-300">
            <i class="ph-bold ph-sign-out text-lg"></i>
          </button>
        </div>
      </div>
    </aside>

    <!-- MAIN CONTENT AREA -->
    <main class="flex-1 h-full overflow-y-auto overflow-x-hidden relative">
      <!-- Mobile Header -->
      <header class="lg:hidden flex items-center justify-between p-6 pb-2">
        <div class="flex items-center gap-3">
          <button @click="toggleSidebar" class="py-2 px-3 rounded-xl bg-white dark:bg-dark-card shadow-sm border border-gray-200 dark:border-gray-700 text-gray-600 dark:text-gray-300">
            <i class="ph-bold ph-list text-xl"></i>
          </button>
          <h2 class="text-xl font-bold dark:text-white">{{ currentPageTitle }}</h2>
        </div>
        <div class="w-10 h-10 rounded-full overflow-hidden border-2 border-primary-500">
          <img src="https://ui-avatars.com/api/?name=Dimas+Rizky&background=4900c7&color=fff" alt="User">
        </div>
      </header>

      <div class="p-6 lg:p-10 max-w-8xl mx-auto">
        <!-- TOP BAR -->
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-10">
          <div>
            <h2 class="text-3xl font-bold text-gray-900 dark:text-white tracking-tight">{{ currentHeader.title }}</h2>
            <p class="text-gray-500 dark:text-dark-muted mt-1">{{ currentHeader.subtitle }}</p>
          </div>

          <div class="flex items-center gap-3">
            <button @click="toggleDarkMode" class="px-4 py-3 rounded-2xl bg-white dark:bg-dark-card shadow-soft border border-gray-100 dark:border-gray-700 text-gray-500 hover:text-primary-500 transition-all duration-300">
              <i :class="isDarkMode? 'ph-bold ph-sun' : 'ph-bold ph-moon'"></i>
            </button>

            <button @click="openNewTaskModal" class="flex items-center gap-2 bg-primary-500 hover:bg-primary-600 text-white px-6 py-4 lg:px-4 lg:py-3 rounded-2xl font-semibold shadow-glow transition-all duration-300 transform hover:-translate-y-1">
              <i class="ph-bold ph-plus"></i>
              <span class="hidden sm:inline">Tugas Baru</span>
            </button>
          </div>
        </div>

        <!-- DASHBOARD PAGE -->
        <div v-show="currentPage === 'dashboard'" class="animate-fade-in">
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-10">
            <div class="bg-white dark:bg-dark-card p-6 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800 flex items-center gap-5 group hover:border-primary-200 dark:hover:border-primary-900 transition-all duration-300">
              <div class="w-16 h-16 rounded-2xl bg-blue-50 dark:bg-blue-900/20 flex items-center justify-center text-blue-500 group-hover:scale-110 transition-all duration-300">
                <i class="ph-duotone ph-list-checks text-3xl"></i>
              </div>
              <div>
                <p class="text-sm font-medium text-gray-500 dark:text-gray-400">Total Tugas</p>
                <h3 class="text-3xl font-bold text-gray-900 dark:text-white mt-1">{{ stats.total }}</h3>
              </div>
            </div>
            <div class="bg-white dark:bg-dark-card p-6 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800 flex items-center gap-5 group hover:border-primary-200 dark:hover:border-primary-900 transition-all duration-300">
              <div class="w-16 h-16 rounded-2xl bg-orange-50 dark:bg-orange-900/20 flex items-center justify-center text-orange-500 group-hover:scale-110 transition-all duration-300">
                <i class="ph-duotone ph-clock-countdown text-3xl"></i>
              </div>
              <div>
                <p class="text-sm font-medium text-gray-500 dark:text-gray-400">Sedang Berjalan</p>
                <h3 class="text-3xl font-bold text-gray-900 dark:text-white mt-1">{{ stats.inProgress }}</h3>
              </div>
            </div>
            <div class="bg-white dark:bg-dark-card p-6 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800 flex items-center gap-5 group hover:border-primary-200 dark:hover:border-primary-900 transition-all duration-300">
              <div class="w-16 h-16 rounded-2xl bg-primary-50 dark:bg-primary-500/10 flex items-center justify-center text-primary-500 group-hover:scale-110 transition-all duration-300">
                <i class="ph-duotone ph-trophy text-3xl"></i>
              </div>
              <div>
                <p class="text-sm font-medium text-gray-500 dark:text-gray-400">Selesai</p>
                <h3 class="text-3xl font-bold text-gray-900 dark:text-white mt-1">{{ stats.completed }}</h3>
              </div>
            </div>
          </div>

          <div class="grid grid-cols-1 xl:grid-cols-3 gap-8">
            <div class="xl:col-span-2 space-y-8">
              <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-6">Progres Analitik</h3>
                <div class="h-[250px] w-full">
                  <canvas ref="productivityChart"></canvas>
                </div>
              </div>
              <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-6">Tugas Terbaru</h3>
                <div class="space-y-4">
                  <div v-for="task in recentTasks" :key="task.id" class="flex items-center p-4 rounded-2xl bg-gray-50 dark:bg-gray-800/50">
                    <div :class="task.iconBg" class="w-10 h-10 rounded-full flex items-center justify-center mr-4">
                      <i :class="task.icon"></i>
                    </div>
                    <div>
                      <h4 class="font-bold dark:text-white">{{ task.title }}</h4>
                      <p class="text-xs text-gray-500">Deadline: {{ task.deadline }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="space-y-8">
              <div class="bg-primary-500 text-white p-8 rounded-[2rem] shadow-glow relative overflow-hidden">
                <div class="absolute -top-10 -right-10 w-40 h-40 bg-white/10 rounded-full blur-2xl"></div>
                <h3 class="text-lg font-bold relative z-10">Desember 2024</h3>
                <div class="grid grid-cols-7 text-center text-xs opacity-70 mt-4 mb-2">
                  <span v-for="day in ['S','S','R','K','J','S','M']" :key="day">{{ day }}</span>
                </div>
                <div class="grid grid-cols-7 text-center gap-2 text-sm relative z-10">
                  <span class="opacity-30">29</span>
                  <span class="opacity-30">30</span>
                  <span>1</span>
                  <span>2</span>
                  <span class="bg-white text-primary-600 rounded-lg shadow-md">3</span>
                  <span>4</span>
                  <span>5</span>
                </div>
              </div>
              <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800">
                <h3 class="font-bold text-gray-900 dark:text-white mb-4">Aktivitas</h3>
                <div class="space-y-4 text-sm text-gray-500 dark:text-gray-400">
                  <p>• <strong class="text-gray-800 dark:text-gray-200">Dimas</strong> upload file baru.</p>
                  <p>• Task "Desain" selesai.</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- TASKS PAGE -->
        <div v-show="currentPage === 'tasks'" class="animate-fade-in">
          <div class="bg-white dark:bg-dark-card p-1 rounded-2xl inline-flex mb-8 border border-gray-100 dark:border-gray-700">
            <button
              v-for="filter in taskFilters"
              :key="filter"
              @click="currentTaskFilter = filter"
              class="px-6 py-2 rounded-xl text-sm font-medium transition-all duration-300"
              :class="currentTaskFilter === filter? 'bg-primary-500 text-white shadow-md' : 'text-gray-500 dark:text-gray-400 hover:text-primary-500'"
            >
              {{ filter }}
            </button>
          </div>

          <div class="space-y-4">
            <div v-for="task in filteredTasks" :key="task.id" class="flex flex-col md:flex-row md:items-center p-6 rounded-[2rem] bg-white dark:bg-dark-card border border-gray-100 dark:border-gray-800 shadow-soft group hover:border-primary-200 dark:hover:border-primary-900 transition-all duration-300">
              <label class="custom-checkbox flex items-center cursor-pointer mb-4 md:mb-0">
                <input type="checkbox" v-model="task.completed" class="sr-only" @change="toggleTask(task)">
                <div class="w-6 h-6 border-2 border-gray-300 dark:border-gray-600 rounded-lg flex items-center justify-center transition-colors" :class="{ 'bg-primary-500 border-primary-500': task.completed }">
                  <svg v-if="task.completed" class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path>
                  </svg>
                </div>
              </label>
              <div class="ml-0 md:ml-6 flex-1">
                <h4 class="text-lg font-bold text-gray-900 dark:text-white" :class="{ 'line-through opacity-60': task.completed }">{{ task.title }}</h4>
                <p class="text-gray-500 text-sm mt-1">{{ task.description }}</p>
                <div class="flex items-center gap-4 mt-3">
                  <div class="flex -space-x-2">
                    <img v-for="member in task.members" :key="member" class="w-8 h-8 rounded-full border-2 border-white dark:border-dark-card" :src="`https://ui-avatars.com/api/?name=${member}&bg=random`" :alt="member">
                  </div>
                  <span class="text-xs font-semibold px-3 py-1 rounded-lg" :class="task.priorityClass">{{ task.priority }}</span>
                </div>
              </div>
              <div class="mt-4 md:mt-0 text-right">
                <p class="text-sm font-bold text-gray-900 dark:text-white">{{ task.deadlineLabel }}</p>
                <p class="text-xs text-gray-400">{{ task.deadlineTime }}</p>
              </div>
            </div>
          </div>
        </div>

        <!-- CALENDAR PAGE -->
        <div v-show="currentPage === 'calendar'" class="animate-fade-in">
          <div class="bg-white dark:bg-dark-card rounded-[2rem] p-8 shadow-soft border border-gray-100 dark:border-gray-800">
            <div class="flex justify-between items-center mb-8">
              <h2 class="text-2xl font-bold dark:text-white">{{ currentMonth }} {{ currentYear }}</h2>
              <div class="flex gap-2">
                <button @click="goToToday" class="px-4 py-2 rounded-xl border dark:border-gray-600 hover:bg-gray-50 dark:hover:bg-gray-700 dark:text-white">Today</button>
                <div class="flex bg-gray-100 dark:bg-gray-700 rounded-xl">
                  <button @click="prevMonth" class="px-3 py-2 hover:bg-gray-200 dark:hover:bg-gray-600 rounded-l-xl dark:text-white"><i class="ph-bold ph-caret-left"></i></button>
                  <button @click="nextMonth" class="px-3 py-2 hover:bg-gray-200 dark:hover:bg-gray-600 rounded-r-xl dark:text-white"><i class="ph-bold ph-caret-right"></i></button>
                </div>
              </div>
            </div>
            <div class="grid grid-cols-7 border-b dark:border-gray-700 pb-4 mb-4 text-center font-bold text-gray-500">
              <div v-for="day in ['Sen','Sel','Rab','Kam','Jum','Sab','Min']" :key="day">{{ day }}</div>
            </div>
            <div class="grid grid-cols-7 gap-4 text-center min-h-[500px]">
              <div v-for="(day, index) in calendarDays" :key="index"
                class="p-2 relative cursor-pointer transition-all duration-300 hover:bg-gray-50 dark:hover:bg-gray-800 rounded-xl"
                :class="{ 'text-gray-300':!day.currentMonth, 'dark:text-white': day.currentMonth, 'bg-primary-500 text-white shadow-glow': day.isToday }"
              >
                {{ day.date }}
                <div v-if="day.hasEvent" class="absolute bottom-2 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-white rounded-full"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- ANALYTICS PAGE -->
        <div v-show="currentPage === 'analytics'" class="animate-fade-in">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800">
              <h3 class="text-lg font-bold mb-4 dark:text-white">Penyelesaian Tugas</h3>
              <div class="h-64 flex items-center justify-center text-gray-400 bg-gray-50 dark:bg-gray-800 rounded-xl">
                Chart Placeholder 1
              </div>
            </div>
            <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800">
              <h3 class="text-lg font-bold mb-4 dark:text-white">Efisiensi Tim</h3>
              <div class="h-64 flex items-center justify-center text-gray-400 bg-gray-50 dark:bg-gray-800 rounded-xl">
                Chart Placeholder 2
              </div>
            </div>
          </div>
        </div>

        <!-- TEAM PAGE -->
        <div v-show="currentPage === 'team'" class="animate-fade-in">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div v-for="member in teamMembers" :key="member.name" class="bg-white dark:bg-dark-card p-6 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800 text-center">
              <img :src="`https://ui-avatars.com/api/?name=${encodeURIComponent(member.name)}&background=${member.avatarColor || '4900c7'}&color=fff`" class="w-20 h-20 rounded-full mx-auto mb-4 border-4 border-primary-50 dark:border-gray-700">
              <h3 class="text-lg font-bold dark:text-white">{{ member.name }}</h3>
              <p class="text-primary-500 text-sm font-medium mb-4">{{ member.role }}</p>
              <div class="flex justify-center gap-2">
                <button class="p-2 rounded-full bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-300"><i class="ph-bold ph-envelope"></i></button>
                <button v-if="member.phone" class="p-2 rounded-full bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-300"><i class="ph-bold ph-phone"></i></button>
              </div>
            </div>
          </div>
        </div>

        <!-- SETTINGS PAGE -->
        <div v-show="currentPage === 'settings'" class="animate-fade-in">
          <div class="bg-white dark:bg-dark-card p-8 rounded-[2rem] shadow-soft border border-gray-100 dark:border-gray-800 max-w-2xl">
            <h3 class="text-xl font-bold dark:text-white mb-6">Pengaturan Profil</h3>
            <div class="space-y-6">
              <div>
                <label class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">Nama Lengkap</label>
                <input type="text" v-model="userProfile.name" class="w-full px-4 py-3 rounded-xl bg-gray-50 dark:bg-gray-800 border-transparent focus:border-primary-500 focus:ring-0 text-gray-900 dark:text-white">
              </div>
              <div>
                <label class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-2">Email</label>
                <input type="email" v-model="userProfile.email" class="w-full px-4 py-3 rounded-xl bg-gray-50 dark:bg-gray-800 border-transparent focus:border-primary-500 focus:ring-0 text-gray-900 dark:text-white">
              </div>
              <div class="flex items-center justify-between py-4 border-t border-gray-100 dark:border-gray-700">
                <div>
                  <h4 class="font-bold dark:text-white">Notifikasi Email</h4>
                  <p class="text-xs text-gray-500">Terima update harian tentang tugas.</p>
                </div>
                <label class="relative inline-flex items-center cursor-pointer">
                  <input type="checkbox" v-model="userProfile.notifications" class="sr-only peer">
                  <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-primary-500"></div>
                </label>
              </div>
              <button @click="saveSettings" class="w-full py-3 rounded-xl bg-primary-500 text-white font-bold shadow-glow hover:bg-primary-600 transition-all duration-300">Simpan Perubahan</button>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'TaskifyApp',
  data() {
    return {
      isSidebarOpen: false,
      isMobile: false,
      isDarkMode: false,
      currentPage: 'dashboard',
      currentPageTitle: 'Dashboard',
      myChart: null,
      menuItems: [
        { id: 'dashboard', label: 'Dashboard', icon: 'ph-bold ph-squares-four' },
        { id: 'tasks', label: 'Tugas', icon: 'ph-bold ph-list-checks', badge: '5' },
        { id: 'calendar', label: 'Kalender', icon: 'ph-bold ph-calendar' },
        { id: 'analytics', label: 'Analitik', icon: 'ph-bold ph-chart-bar' },
        { id: 'team', label: 'Tim', icon: 'ph-bold ph-users' },
        { id: 'settings', label: 'Pengaturan', icon: 'ph-bold ph-gear' },
      ],
      currentHeader: {
        title: 'Selamat Datang, Dimas!',
        subtitle: 'Mari selesaikan tugasmu hari ini'
      },
      stats: {
        total: 24,
        inProgress: 8,
        completed: 16
      },
      taskFilters: ['Semua', 'Aktif', 'Selesai'],
      currentTaskFilter: 'Semua',
      recentTasks: [
        { id: 1, title: 'Desain UI Dashboard', deadline: '3 Des 2024', icon: 'ph-bold ph-paint-brush text-white', iconBg: 'bg-blue-500' },
        { id: 2, title: 'Fix Bug Login', deadline: '5 Des 2024', icon: 'ph-bold ph-bug text-white', iconBg: 'bg-red-500' },
        { id: 3, title: 'Meeting Client', deadline: '7 Des 2024', icon: 'ph-bold ph-users text-white', iconBg: 'bg-green-500' },
      ],
      allTasks: [
        { id: 1, title: 'Buat Wireframe Landing Page', description: 'Siapkan wireframe untuk client ABC', completed: false, members: ['Dimas', 'Sari'], priority: 'Tinggi', priorityClass: 'bg-red-100 text-red-700 dark:bg-red-900/30 dark:text-red-400', deadlineLabel: 'Besok', deadlineTime: '10:00 AM' },
        { id: 2, title: 'Review Code PR #124', description: 'Check pull request dari tim backend', completed: false, members: ['Budi'], priority: 'Sedang', priorityClass: 'bg-orange-100 text-orange-700 dark:bg-orange-900/30 dark:text-orange-400', deadlineLabel: '5 Des', deadlineTime: '17:00 PM' },
        { id: 3, title: 'Deploy ke Staging', description: 'Deploy versi 2.1.0 ke server staging', completed: true, members: ['Dimas'], priority: 'Rendah', priorityClass: 'bg-green-100 text-green-700 dark:bg-green-900/30 dark:text-green-400', deadlineLabel: 'Selesai', deadlineTime: '1 Des' },
      ],
      calendarDays: [
        { date: 29, currentMonth: false, isToday: false, hasEvent: false },
        { date: 30, currentMonth: false, isToday: false, hasEvent: false },
        { date: 1, currentMonth: true, isToday: false, hasEvent: false },
        { date: 2, currentMonth: true, isToday: false, hasEvent: true },
        { date: 3, currentMonth: true, isToday: true, hasEvent: false },
        { date: 4, currentMonth: true, isToday: false, hasEvent: false },
        { date: 5, currentMonth: true, isToday: false, hasEvent: true },
      ],
      currentMonth: 'Desember',
      currentYear: 2024,
      teamMembers: [
        { name: 'Dimas Rizky', role: 'Lead Developer', avatarColor: '4900c7', phone: true },
        { name: 'Sari Putri', role: 'UI/UX Designer', avatarColor: 'ec4899', phone: false },
        { name: 'Budi Santoso', role: 'Backend Dev', avatarColor: 'f59e0b', phone: true },
        { name: 'Andi Wijaya', role: 'QA Engineer', avatarColor: '10b981', phone: false },
      ],
      userProfile: {
        name: 'Dimas Rizky',
        email: 'dimas@taskify.com',
        notifications: true
      },
    }
  },

  computed: {
    sidebarClasses() {
      if (this.isMobile) {
        return this.isSidebarOpen? 'translate-x-0' : '-translate-x-full'
      } else {
        return 'translate-x-0'
      }
    },
    activeClasses() {
      return 'bg-primary-500 text-white shadow-glow'
    },
    inactiveClasses() {
      return 'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800 hover:text-gray-900 dark:hover:text-white'
    },
    filteredTasks() {
      if (this.currentTaskFilter === 'Aktif') return this.allTasks.filter(t =>!t.completed)
      if (this.currentTaskFilter === 'Selesai') return this.allTasks.filter(t => t.completed)
      return this.allTasks
    }
  },

  mounted() {
    this.initDarkMode()
    this.initChart()
    this.checkMobile()
    window.addEventListener('resize', this.checkMobile)
    window.addEventListener('resize', this.handleResize)
  },

  beforeUnmount() {
    if (this.myChart) {
      this.myChart.destroy()
    }
    window.removeEventListener('resize', this.checkMobile)
    window.removeEventListener('resize', this.handleResize)
  },

  methods: {
    checkMobile() {
      this.isMobile = window.innerWidth < 1024
      if (!this.isMobile) {
        this.isSidebarOpen = false
      }
    },
    handleResize() {},
    toggleSidebar() {
      if (this.isMobile) {
        this.isSidebarOpen =!this.isSidebarOpen
      }
    },
    switchPage(pageId) {
      this.currentPage = pageId
      const page = this.menuItems.find(item => item.id === pageId)
      this.currentPageTitle = page? page.label : 'Dashboard'
      this.updateHeader(pageId)
      if (this.isMobile && this.isSidebarOpen) {
        this.toggleSidebar()
      }
    },
    updateHeader(pageId) {
      const headers = {
        dashboard: { title: 'Selamat Datang, Dimas!', subtitle: 'Mari selesaikan tugasmu hari ini' },
        tasks: { title: 'Daftar Tugas', subtitle: 'Kelola semua tugasmu di sini' },
        calendar: { title: 'Kalender', subtitle: 'Lihat jadwal dan deadline' },
        analytics: { title: 'Analitik', subtitle: 'Pantau progres tim kamu' },
        team: { title: 'Anggota Tim', subtitle: 'Kolaborasi dengan tim kamu' },
        settings: { title: 'Pengaturan', subtitle: 'Atur preferensi akun kamu' }
      }
      this.currentHeader = headers[pageId] || headers.dashboard
    },
    initDarkMode() {
      this.isDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches
      this.applyDarkMode()
    },
    toggleDarkMode() {
      this.isDarkMode =!this.isDarkMode
      this.applyDarkMode()
    },
    applyDarkMode() {
      if (this.isDarkMode) {
        document.documentElement.classList.add('dark')
      } else {
        document.documentElement.classList.remove('dark')
      }
    },
    initChart() {
      // Placeholder pour Chart.js
      console.log('Chart init')
    },
    openNewTaskModal() {
      alert('Modal Tugas Baru - à implémenter')
    },
    toggleTask(task) {
      if (task.completed) {
        this.stats.completed++
        this.stats.inProgress--
      } else {
        this.stats.completed--
        this.stats.inProgress++
      }
    },
    logout() {
      alert('Logout - à implémenter')
    },
    goToToday() {
      console.log('Go to today')
    },
    prevMonth() {
      console.log('Prev month')
    },
    nextMonth() {
      console.log('Next month')
    },
    saveSettings() {
      alert('Pengaturan disimpan!')
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap');
@import url('https://unpkg.com/@phosphor-icons/web@2.0.3/src/css/icons.css');

* {
  font-family: 'Plus Jakarta Sans', sans-serif;
}

.animate-fade-in {
  animation: fadeIn 0.5s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.shadow-soft {
  box-shadow: 0 4px 20px -2px rgba(73, 0, 199, 0.05);
}

.shadow-glow {
  box-shadow: 0 0 15px rgba(73, 0, 199, 0.3);
}

.trans-all {
  transition: all 0.3s ease;
}

/* Couleurs Tailwind custom si tu n'as pas tailwind.config.js */
/* .bg-primary-500 { background-color: #4900c7; }
.bg-primary-600 { background-color: #3d00a8; }
.bg-primary-50 { background-color: #f5f0ff; }
.bg-primary-100 { background-color: #e6d9ff; }
.bg-primary-900 { background-color: #2a006e; }
.text-primary-500 { color: #4900c7; }
.text-primary-600 { color: #3d00a8; }
.text-primary-700 { color: #2a006e; }
.text-primary-300 { color: #c4a8ff; }
.border-primary-500 { border-color: #4900c7; }
.border-primary-200 { border-color: #d4c2ff; }
.border-primary-900 { border-color: #2a006e; }
.hover\\:bg-primary-600:hover { background-color: #3d00a8; }
.hover\\:text-primary-500:hover { color: #4900c7; }
.hover\\:border-primary-200:hover { border-color: #d4c2ff; }
.dark\\:hover\\:border-primary-900:hover { border-color: #2a006e; }
.dark\\:bg-dark-card { background-color: #1a1a1a; }
.dark\\:text-dark-muted { color: #9ca3af; } */
</style>
