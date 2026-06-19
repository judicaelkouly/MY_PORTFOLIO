Voici votre fichier Vue.js complet et autonome, prêt à être utilisé dans un projet Vue CLI, Vite ou Nuxt.

```vue
<template>
  <div @mousemove="handleMouseMove">
    <!-- animated background particles + lightning -->
    <div class="bg-animation" style="position:fixed; top:0; left:0; width:100%; height:100%; pointer-events:none; z-index:0; overflow:hidden">
      <canvas id="particleCanvas" style="position:absolute; top:0; left:0; width:100%; height:100%"></canvas>
      <div id="lightning" style="position:absolute; top:0; left:0; width:100%; height:100%; background: radial-gradient(circle, rgba(124,58,237,0.3) 0%, rgba(0,0,0,0) 80%); opacity:0; pointer-events:none; transition: opacity 0.05s linear;"></div>
      <div style="position:absolute; top:0; left:50%; transform:translateX(-50%); width:80%; height:400px; background: radial-gradient(ellipse, rgba(124,58,237,0.06) 0%, transparent 70%); pointer-events:none;"></div>
    </div>

    <!-- custom cursor -->
    <div class="cursor-dot" ref="dot"></div>
    <div class="cursor-ring" ref="ring"></div>

    <nav class="glass-nav">
      <div class="nav-container">
        <div class="logo">Alex<span>.</span>dev</div>
        <div class="nav-links">
          <a v-for="item in navItems" :key="item" href="#" @click.prevent="scrollTo(item.toLowerCase())" :class="{active: activeSection === item.toLowerCase()}">{{ item }}</a>
        </div>
        <button class="hire-btn" @click="scrollTo('contact')">Hire Me</button>
        <div class="burger">☰</div>
      </div>
    </nav>

    <main>
      <!-- Hero -->
      <section id="home" class="hero">
        <div class="container reveal">
          <div class="status-badge"><span class="pulse-dot"></span> Open to work · Remote & On-site</div>
          <div class="hero-title">
            Full Stack<br>
            <span style="color:#7C3AED">Developer &</span><br>
            <span style="color:#06B6D4">Problem Solver</span>
          </div>
          <div class="hero-desc">I craft modern, scalable web applications — from pixel-perfect interfaces to robust backend architectures.</div>
          <div class="cta-group">
            <button class="btn-primary magnetic" @click="scrollTo('projects')">View Projects →</button>
            <button class="btn-secondary magnetic" @click="scrollTo('contact')">Let's Talk</button>
          </div>
          <div class="tech-pills">
            <div v-for="tech in techStack" :key="tech.name" class="tech-pill" :style="{animation: 'subtleFloat 3s infinite ease-in-out', animationDelay: tech.delay}"><span class="color-dot" :style="{background: tech.color}"></span> {{ tech.name }}</div>
          </div>
        </div>
      </section>

      <!-- About -->
      <section id="about">
        <div class="container reveal">
          <div class="section-label">ABOUT</div>
          <div class="section-title">Turning ideas into living products</div>
          <div class="stats-grid">
            <div v-for="stat in stats" :key="stat.label" class="stat-card magnetic">
              <div class="stat-number"><span>{{ stat.animatedValue }}</span>+</div>
              <div class="stat-label">{{ stat.label }}</div>
            </div>
          </div>
        </div>
      </section>

      <!-- Skills -->
      <section id="skills">
        <div class="container reveal">
          <div class="section-label">EXPERTISE</div>
          <div class="section-title">Tech toolkit</div>
          <div class="filters">
            <button v-for="filter in skillFilters" :key="filter" @click="activeSkillFilter=filter" class="filter-btn" :class="{active: activeSkillFilter === filter}">{{ filter }}</button>
          </div>
          <div class="tech-pills" style="gap: 10px;">
            <div v-for="skill in filteredSkills" :key="skill.name" class="skill-pill tech-pill" style="cursor:pointer;"><span>{{ skill.emoji }}</span> {{ skill.name }}</div>
          </div>
        </div>
      </section>

      <!-- Projects (cyan filters) -->
      <section id="projects" class="cyan-active">
        <div class="container reveal">
          <div class="section-label">PORTFOLIO</div>
          <div class="section-title">Selected works</div>
          <div class="filters">
            <button v-for="filter in projectFilters" :key="filter" @click="activeProjectFilter=filter" class="filter-btn" :class="{active: activeProjectFilter === filter}">{{ filter }}</button>
          </div>
          <div class="projects-grid">
            <div v-for="proj in filteredProjects" :key="proj.title" class="project-card magnetic" @mouseenter="applyTilt($event)" @mouseleave="resetTilt($event)">
              <div class="project-thumb" :style="{background: proj.bg}">{{ proj.emoji }}</div>
              <div style="padding:18px">
                <div style="font-weight:700">{{ proj.title }}</div>
                <div style="font-size:12px; color:#8B899A; margin:8px 0;">{{ proj.desc }}</div>
                <div style="display:flex; gap:6px; flex-wrap:wrap; margin:12px 0;">
                  <span v-for="t in proj.tags" :key="t" style="background:#1A1A24; padding:2px 10px; border-radius:20px; font-size:11px;">{{ t }}</span>
                </div>
                <div style="display:flex; gap:12px; margin-top:12px">
                  <button style="color:#10B981; background:transparent; border:none">↗ Live Demo</button>
                  <button style="color:#8B899A; background:transparent; border:none">◎ GitHub</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Timeline -->
      <section id="experience">
        <div class="container reveal">
          <div class="section-label">JOURNEY</div>
          <div class="section-title">Experience & education</div>
          <div class="timeline">
            <div class="timeline-line"></div>
            <div v-for="(exp, idx) in timelineData" :key="idx" class="timeline-item" :style="{transitionDelay: (idx*0.1)+'s'}">
              <div class="timeline-dot"></div>
              <div class="timeline-card" style="background:#111118; border-radius:12px; padding:18px 20px; border:1px solid rgba(255,255,255,0.07); margin-left:20px;">
                <div style="display:flex; justify-content:space-between;"><span style="background:rgba(124,58,237,0.2); padding:2px 10px; border-radius:20px; font-size:11px;">{{ exp.year }}</span><span>{{ exp.type }}</span></div>
                <div style="font-weight:700; margin-top:8px;">{{ exp.role }}</div>
                <div style="color:#06B6D4; font-size:12px;">{{ exp.org }}</div>
                <div style="color:#8B899A; font-size:12px; margin-top:6px;">{{ exp.desc }}</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Testimonials Carousel -->
      <section>
        <div class="container reveal">
          <div class="section-label">TESTIMONIALS</div>
          <div class="section-title">Kind words</div>
          <div style="overflow:hidden; position:relative">
            <div class="carousel-track" :style="{transform: 'translateX(-'+ (testimonialIndex * 100) +'%)'}">
              <div v-for="(t, idx) in testimonials" :key="idx" class="carousel-slide">
                <div class="testimonial-card">
                  <i class="fas fa-quote-left" style="color:#7C3AED; opacity:0.5; margin-bottom:12px; display:block"></i>
                  <div style="font-style:italic; line-height:1.8;">{{ t.quote }}</div>
                  <div style="display:flex; align-items:center; gap:12px; margin-top:20px;">
                    <div style="width:40px; height:40px; background:linear-gradient(135deg, #7C3AED, #06B6D4); border-radius:40px; display:flex; align-items:center; justify-content:center; font-weight:bold;">{{ t.initials }}</div>
                    <div><strong>{{ t.name }}</strong><div style="font-size:12px; color:#8B899A">{{ t.role }}</div></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="carousel-dots">
              <div v-for="(_, idx) in testimonials" :key="idx" class="dot" :class="{active: testimonialIndex === idx}" @click="testimonialIndex = idx"></div>
            </div>
          </div>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact">
        <div class="container reveal">
          <div class="section-label">GET IN TOUCH</div>
          <div class="section-title">Let's build something amazing</div>
          <div class="contact-grid">
            <div>
              <div class="info-card"><i class="fas fa-envelope" style="font-size:24px; color:#7C3AED"></i><div><div style="color:#8B899A; font-size:12px">Email</div><div>alex@devportfolio.com</div></div></div>
              <div class="info-card"><i class="fas fa-phone-alt" style="font-size:24px; color:#06B6D4"></i><div><div style="color:#8B899A; font-size:12px">Phone</div><div>+33 6 12 34 56 78</div></div></div>
              <div class="info-card"><i class="fas fa-map-marker-alt" style="font-size:24px; color:#10B981"></i><div><div style="color:#8B899A; font-size:12px">Location</div><div>Paris / Remote</div></div></div>
              <div class="info-card"><i class="fas fa-clock" style="font-size:24px; color:#F59E0B"></i><div><div style="color:#8B899A; font-size:12px">Availability</div><div>Open for contracts</div></div></div>
            </div>
            <div class="form-card">
              <div class="form-row"><input placeholder="Name" v-model="form.name"><input placeholder="Email" v-model="form.email"></div>
              <input placeholder="Subject" v-model="form.subject" style="margin:16px 0;">
              <textarea rows="4" placeholder="Your message..." v-model="form.message"></textarea>
              <button class="btn-primary" style="width:100%; margin-top:20px;" @click="submitForm">Let's Build Something Amazing ⚡</button>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="container footer">
      <div class="logo">Alex<span>.</span>dev</div>
      <div class="social-icons"><div class="social-icon"><i class="fab fa-github"></i></div><div class="social-icon"><i class="fab fa-linkedin-in"></i></div><div class="social-icon"><i class="fab fa-twitter"></i></div></div>
      <div style="font-size:12px; color:#8B899A">© 2025 — Full Stack Portfolio</div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      activeSection: 'home',
      navItems: ['Home','About','Skills','Projects','Contact'],
      techStack: [
        {name:'React',color:'#61DAFB',delay:'0s'},{name:'Laravel',color:'#FF2D20',delay:'0.1s'},{name:'Node.js',color:'#339933',delay:'0.2s'},
        {name:'Vue.js',color:'#42b883',delay:'0.3s'},{name:'MySQL',color:'#00758F',delay:'0.4s'},{name:'Flutter',color:'#02569B',delay:'0.5s'},
        {name:'TypeScript',color:'#3178C6',delay:'0.6s'},{name:'MongoDB',color:'#47A248',delay:'0.7s'}
      ],
      stats: [
        {label:'Years of Experience', target:4, animatedValue:0},
        {label:'Completed Projects', target:32, animatedValue:0},
        {label:'Happy Clients', target:18, animatedValue:0},
        {label:'Technologies', target:20, animatedValue:0}
      ],
      skillFilters: ['All','Frontend','Backend','Database','Tools'],
      activeSkillFilter: 'All',
      skills: [
        {name:'React', category:'Frontend', emoji:'⚛️'},{name:'Vue', category:'Frontend', emoji:'💚'},{name:'TypeScript', category:'Frontend', emoji:'🔷'},
        {name:'Laravel', category:'Backend', emoji:'🐘'},{name:'Node.js', category:'Backend', emoji:'🟢'},{name:'MySQL', category:'Database', emoji:'🗄️'},
        {name:'MongoDB', category:'Database', emoji:'🍃'},{name:'Git', category:'Tools', emoji:'📦'},{name:'Docker', category:'Tools', emoji:'🐳'}
      ],
      projectFilters: ['All','Web Apps','Mobile','Laravel','React'],
      activeProjectFilter: 'All',
      projects: [
        {title:'SPMB Admin Portal', desc:'Analytics dashboard', tags:['Vue','Tailwind'], category:'Web Apps', emoji:'📊', bg:'rgba(124,58,237,0.2)'},
        {title:'E-Commerce Platform', desc:'Full-stack Laravel', tags:['Laravel','MySQL'], category:'Laravel', emoji:'🛒', bg:'rgba(6,182,212,0.2)'},
        {title:'Task Manager App', desc:'Real-time sync', tags:['React','Socket.io'], category:'React', emoji:'✅', bg:'rgba(16,185,129,0.2)'},
        {title:'Mobile Banking', desc:'Flutter + Firebase', tags:['Flutter'], category:'Mobile', emoji:'📱', bg:'rgba(245,158,11,0.2)'}
      ],
      timelineData: [
        {year:'2025',type:'🎓 Education',role:'Master 1 BCD',org:'UVCI',desc:'Specialized cloud architectures'},
        {year:'2024',type:'💼 Freelance',role:'Full Stack Developer',org:'Self-employed',desc:'Delivered 12+ projects'},
        {year:'2023',type:'🛠 Internship',role:'Frontend Developer',org:'Local Startup',desc:'Built design system'},
        {year:'2022',type:'🎓 Education',role:'Bachelor CS',org:'UVCI',desc:'Graduated with honors'},
        {year:'2021',type:'🏆 Certification',role:'AWS Cloud Practitioner',org:'Amazon',desc:'Cloud fundamental certified'}
      ],
      testimonials: [
        {quote:'Alex transformed our vision into a sleek, performant platform. True expert.', name:'Sophie M.', role:'CTO @ Studio', initials:'SM'},
        {quote:'Code quality and UX thinking is outstanding. Would hire anytime.', name:'Julien R.', role:'Product Lead', initials:'JR'}
      ],
      testimonialIndex: 0,
      form: {name:'',email:'',subject:'',message:''},
      autoSlideInterval: null,
      particlesAnimation: null,
      lightningInterval: null,
      counterIntervals: []
    }
  },
  computed: {
    filteredSkills() {
      if(this.activeSkillFilter === 'All') return this.skills;
      return this.skills.filter(s => s.category === this.activeSkillFilter);
    },
    filteredProjects() {
      if(this.activeProjectFilter === 'All') return this.projects;
      return this.projects.filter(p => p.category === this.activeProjectFilter);
    }
  },
  mounted() {
    this.initParticles();
    this.startAutoSlide();
    this.initScrollReveal();
    this.initCountersOnView();
    this.lightningInterval = setInterval(() => { this.lightningEffect() }, 6000);
  },
  beforeUnmount() {
    if(this.autoSlideInterval) clearInterval(this.autoSlideInterval);
    if(this.lightningInterval) clearInterval(this.lightningInterval);
    if(this.particlesAnimation) cancelAnimationFrame(this.particlesAnimation);
    this.counterIntervals.forEach(interval => clearInterval(interval));
  },
  methods: {
    handleMouseMove(e) {
      if(this.$refs.dot && this.$refs.ring) {
        this.$refs.dot.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
        this.$refs.ring.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
      }
    },
    scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      if(element) {
        element.scrollIntoView({behavior:'smooth'});
        this.activeSection = sectionId;
      }
    },
    initParticles() {
      const canvas = document.getElementById('particleCanvas');
      if(!canvas) return;
      const ctx = canvas.getContext('2d');

      const resizeCanvas = () => {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      };
      resizeCanvas();
      window.addEventListener('resize', resizeCanvas);

      let particles = [];
      for(let i = 0; i < 60; i++) {
        particles.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          radius: Math.random() * 2 + 1,
          vx: (Math.random() - 0.5) * 0.4,
          vy: (Math.random() - 0.5) * 0.2,
          color: `rgba(124,58,237,${Math.random() * 0.4})`
        });
      }

      const animate = () => {
        if(!ctx || !canvas) return;
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        particles.forEach(p => {
          p.x += p.vx;
          p.y += p.vy;
          if(p.x < 0) p.x = canvas.width;
          if(p.x > canvas.width) p.x = 0;
          if(p.y < 0) p.y = canvas.height;
          if(p.y > canvas.height) p.y = 0;
          ctx.beginPath();
          ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
          ctx.fillStyle = p.color;
          ctx.fill();
        });
        this.particlesAnimation = requestAnimationFrame(animate);
      };
      animate();
    },
    lightningEffect() {
      const lightningDiv = document.getElementById('lightning');
      if(lightningDiv) {
        lightningDiv.style.opacity = '0.3';
        setTimeout(() => { if(lightningDiv) lightningDiv.style.opacity = '0'; }, 200);
      }
    },
    startCounter(stat) {
      if(stat.animatedValue >= stat.target) return;
      let current = 0;
      const step = Math.ceil(stat.target / 40);
      const interval = setInterval(() => {
        current += step;
        if(current >= stat.target) {
          current = stat.target;
          clearInterval(interval);
          const index = this.counterIntervals.indexOf(interval);
          if(index > -1) this.counterIntervals.splice(index, 1);
        }
        stat.animatedValue = current;
        this.$forceUpdate();
      }, 30);
      this.counterIntervals.push(interval);
    },
    initCountersOnView() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if(entry.isIntersecting) {
            this.stats.forEach(stat => {
              if(stat.animatedValue === 0) this.startCounter(stat);
            });
          }
        });
      }, {threshold: 0.5});
      const aboutSec = document.getElementById('about');
      if(aboutSec) observer.observe(aboutSec);
    },
    initScrollReveal() {
      const reveals = document.querySelectorAll('.reveal');
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if(entry.isIntersecting) entry.target.classList.add('visible');
        });
      }, {threshold: 0.1});
      reveals.forEach(el => observer.observe(el));
    },
    startAutoSlide() {
      this.autoSlideInterval = setInterval(() => {
        this.testimonialIndex = (this.testimonialIndex + 1) % this.testimonials.length;
      }, 5000);
    },
    applyTilt(e) {
      const card = e.currentTarget;
      card.style.transition = 'transform 0.2s';
      const handleMouseMove = (ev) => {
        const rect = card.getBoundingClientRect();
        const x = ev.clientX - rect.left;
        const y = ev.clientY - rect.top;
        const xRot = ((y / rect.height) - 0.5) * 6;
        const yRot = ((x / rect.width) - 0.5) * -6;
        card.style.transform = `perspective(800px) rotateX(${xRot}deg) rotateY(${yRot}deg) translateY(-4px)`;
      };
      card.addEventListener('mousemove', handleMouseMove);
      card.addEventListener('mouseleave', () => {
        card.style.transform = '';
        card.removeEventListener('mousemove', handleMouseMove);
      }, {once: true});
    },
    resetTilt(e) {
      e.currentTarget.style.transform = '';
    },
    submitForm() {
      alert('Message envoyé (démo). Merci !');
      this.form = {name:'', email:'', subject:'', message:''};
    }
  }
}
</script>

<style scoped>
@keyframes subtleFloat {
  0% { transform: translateY(0px); }
  100% { transform: translateY(-5px); }
}

@keyframes pulse {
  0% { opacity: 1; transform: scale(1);}
  100% { opacity: 0.4; transform: scale(1.2);}
}

.cursor-dot, .cursor-ring {
  position: fixed;
  top: 0;
  left: 0;
  pointer-events: none;
  z-index: 9999;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: transform 0.1s ease;
}
.cursor-dot {
  width: 8px;
  height: 8px;
  background-color: white;
}
.cursor-ring {
  width: 32px;
  height: 32px;
  background-color: rgba(124,58,237,0.3);
  border: 1px solid rgba(124,58,237,0.6);
  transition: width 0.2s, height 0.2s, background 0.2s;
}

.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
}
section {
  padding: 80px 0;
}
.section-label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #7C3AED;
  margin-bottom: 12px;
}
.section-title {
  font-size: 38px;
  font-weight: 800;
  letter-spacing: -1px;
  margin-bottom: 16px;
}
.glass-nav {
  background: rgba(10,10,15,0.75);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(255,255,255,0.07);
  position: sticky;
  top: 0;
  z-index: 100;
  height: 56px;
  display: flex;
  align-items: center;
}
.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
}
.logo {
  font-size: 16px;
  font-weight: 700;
}
.logo span {
  color: #7C3AED;
}
.nav-links {
  display: flex;
  gap: 28px;
  background: transparent;
}
.nav-links a {
  text-decoration: none;
  color: #8B899A;
  font-size: 14px;
  font-weight: 500;
  transition: 0.2s;
  padding: 6px 12px;
  border-radius: 8px;
  cursor: pointer;
}
.nav-links a.active, .nav-links a:hover {
  color: white;
  background: #1A1A24;
}
.hire-btn {
  background: #7C3AED;
  padding: 8px 20px;
  border-radius: 10px;
  color: white;
  font-weight: 600;
  box-shadow: 0 0 12px rgba(124,58,237,0.3);
  transition: 0.2s;
  border: none;
  cursor: pointer;
}
.hire-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 24px rgba(124,58,237,0.5);
}
.hero {
  min-height: calc(100vh - 56px);
  display: flex;
  align-items: center;
}
.status-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(124,58,237,0.12);
  border: 1px solid rgba(124,58,237,0.3);
  border-radius: 20px;
  padding: 6px 14px;
  font-size: 12px;
  font-weight: 500;
  color: #A78BFA;
  margin-bottom: 24px;
}
.pulse-dot {
  width: 8px;
  height: 8px;
  background: #10B981;
  border-radius: 50%;
  display: inline-block;
  animation: pulse 1.5s infinite;
}
.hero-title {
  font-size: 54px;
  font-weight: 800;
  letter-spacing: -1.5px;
  line-height: 1.1;
  margin-bottom: 20px;
}
.hero-desc {
  font-size: 16px;
  color: #8B899A;
  max-width: 460px;
  margin-bottom: 32px;
}
.cta-group {
  display: flex;
  gap: 12px;
  margin-bottom: 40px;
}
.btn-primary {
  background: #7C3AED;
  padding: 12px 24px;
  border-radius: 10px;
  font-weight: 600;
  box-shadow: 0 0 24px rgba(124,58,237,0.3);
  transition: 0.2s;
  border: none;
  color: white;
  cursor: pointer;
}
.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 40px rgba(124,58,237,0.5);
}
.btn-secondary {
  background: transparent;
  border: 1px solid rgba(255,255,255,0.2);
  padding: 12px 24px;
  border-radius: 10px;
  font-weight: 600;
  transition: 0.2s;
  cursor: pointer;
  color: #E8E6F0;
}
.btn-secondary:hover {
  background: #1A1A24;
}
.tech-pills {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}
.tech-pill {
  background: #111118;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 24px;
  padding: 6px 16px;
  font-size: 12px;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: 0.2s;
}
.tech-pill:hover {
  border-color: #7C3AED;
  box-shadow: 0 0 12px rgba(124,58,237,0.3);
  transform: translateY(-2px);
}
.color-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  display: inline-block;
}
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 48px;
}
.stat-card {
  background: #111118;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 14px;
  padding: 24px 20px;
  text-align: center;
  transition: 0.3s;
}
.stat-card:hover {
  border-color: rgba(124,58,237,0.4);
  transform: translateY(-3px);
  box-shadow: 0 0 24px rgba(124,58,237,0.12);
}
.stat-number {
  font-size: 32px;
  font-weight: 800;
  background: linear-gradient(135deg, #7C3AED, #06B6D4);
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}
.stat-label {
  font-size: 12px;
  color: #8B899A;
  margin-top: 8px;
}
.filters {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-bottom: 40px;
}
.filter-btn {
  background: #111118;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 8px;
  padding: 6px 14px;
  font-size: 12px;
  transition: 0.2s;
  cursor: pointer;
  color: #8B899A;
}
.filter-btn.active {
  background: rgba(124,58,237,0.15);
  border-color: rgba(124,58,237,0.4);
  color: #A78BFA;
}
.cyan-active .filter-btn.active {
  background: rgba(6,182,212,0.15);
  border-color: rgba(6,182,212,0.4);
  color: #06B6D4;
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
}
.project-card {
  background: #111118;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 16px;
  overflow: hidden;
  transition: all 0.3s cubic-bezier(0.2, 0.9, 0.4, 1.1);
  transform-style: preserve-3d;
}
.project-card:hover {
  border-color: rgba(6,182,212,0.4);
  transform: translateY(-4px);
  box-shadow: 0 16px 48px rgba(6,182,212,0.12);
}
.project-thumb {
  height: 130px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 48px;
}
.timeline {
  position: relative;
  padding-left: 24px;
}
.timeline-line {
  position: absolute;
  left: 8px;
  top: 0;
  width: 1px;
  height: 100%;
  background: rgba(255,255,255,0.07);
}
.timeline-item {
  position: relative;
  margin-bottom: 28px;
  transition: all 0.3s;
}
.timeline-dot {
  position: absolute;
  left: -20px;
  top: 20px;
  width: 10px;
  height: 10px;
  background: #7C3AED;
  border-radius: 50%;
  box-shadow: 0 0 8px #7C3AED;
}
.timeline-card {
  transition: 0.3s;
}
.timeline-card:hover {
  border-color: rgba(124,58,237,0.4) !important;
  transform: translateX(4px);
}
.testimonial-card {
  background: rgba(10,10,15,0.75);
  backdrop-filter: blur(16px);
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 16px;
  padding: 28px;
  margin: 16px;
}
.carousel-track {
  display: flex;
  transition: transform 0.5s cubic-bezier(0.2, 0.9, 0.4, 1.1);
}
.carousel-slide {
  min-width: 100%;
  padding: 0 12px;
}
.carousel-dots {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin-top: 24px;
}
.dot {
  width: 6px;
  height: 6px;
  background: #2a2a33;
  border-radius: 6px;
  transition: 0.3s;
  cursor: pointer;
}
.dot.active {
  width: 20px;
  background: #7C3AED;
  border-radius: 3px;
}
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1.4fr;
  gap: 32px;
}
.info-card {
  background: #111118;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 12px;
  padding: 16px;
  display: flex;
  gap: 16px;
  margin-bottom: 16px;
  transition: 0.3s;
}
.info-card:hover {
  border-color: rgba(124,58,237,0.4);
  transform: translateY(-2px);
}
.form-card {
  background: #111118;
  border-radius: 16px;
  padding: 24px;
  border: 1px solid rgba(255,255,255,0.07);
}
input, textarea {
  background: #1A1A24;
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 8px;
  padding: 10px 14px;
  width: 100%;
  color: white;
  font-family: inherit;
}
input:focus, textarea:focus {
  outline: none;
  border-color: rgba(124,58,237,0.5);
}
.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}
.footer {
  border-top: 1px solid rgba(255,255,255,0.07);
  padding: 24px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
.social-icons {
  display: flex;
  gap: 12px;
}
.social-icon {
  width: 34px;
  height: 34px;
  background: #111118;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: 0.2s;
  cursor: pointer;
  border: 1px solid rgba(255,255,255,0.07);
}
.social-icon:hover {
  transform: translateY(-2px);
  border-color: #7C3AED;
}
.burger {
  display: none;
  font-size: 24px;
  cursor: pointer;
}

@media (max-width: 768px) {
  .hero-title { font-size: 38px; }
  .contact-grid { grid-template-columns: 1fr; }
  .nav-links { display: none; }
  .burger { display: block; }
  .timeline { padding-left: 16px; }
  .section-title { font-size: 28px; }
  section { padding: 60px 0; }
  .form-row { grid-template-columns: 1fr; }
}
</style>
