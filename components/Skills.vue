<template>
  <section id="skills" class="py-20 md:py-32 px-6 relative overflow-hidden">
    <!-- Animated Background with Floating Orbs -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900">
      <!-- Floating gradient orbs -->
      <div class="absolute top-20 left-10 w-96 h-96 bg-blue-400/20 dark:bg-blue-600/10 rounded-full blur-3xl animate-float-slow"></div>
      <div class="absolute bottom-20 right-10 w-80 h-80 bg-purple-400/20 dark:bg-purple-600/10 rounded-full blur-3xl animate-float-medium"></div>
      <div class="absolute top-1/2 left-1/2 w-72 h-72 bg-cyan-400/20 dark:bg-cyan-600/10 rounded-full blur-3xl animate-float-fast"></div>
      
      <!-- Animated particles -->
      <div class="absolute inset-0 overflow-hidden">
        <div v-for="i in 20" :key="i" 
             class="absolute w-1 h-1 bg-blue-400/30 dark:bg-blue-500/20 rounded-full animate-particle"
             :style="{
               left: `${Math.random() * 100}%`,
               top: `${Math.random() * 100}%`,
               animationDelay: `${Math.random() * 5}s`,
               animationDuration: `${3 + Math.random() * 4}s`
             }">
        </div>
      </div>
      
      <!-- Grid pattern overlay -->
      <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808012_1px,transparent_1px),linear-gradient(to_bottom,#80808012_1px,transparent_1px)] dark:bg-[linear-gradient(to_right,#ffffff08_1px,transparent_1px),linear-gradient(to_bottom,#ffffff08_1px,transparent_1px)] bg-[size:64px_64px]"></div>
    </div>

    <div class="max-w-7xl mx-auto relative z-10">
      <!-- Section Header with Animation -->
      <div 
        class="text-center mb-16 md:mb-24 animate-fade-in-up"
        :style="{
          opacity: scrollProgress,
          transform: `translateY(${(1 - scrollProgress) * 50}px)`
        }">
        <div class="inline-flex items-center gap-3 px-6 py-3 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-md text-slate-700 dark:text-slate-300 text-sm font-medium border border-slate-200/50 dark:border-slate-700/50 shadow-lg mb-8 hover:scale-105 transition-transform duration-300">
          <span class="text-2xl animate-bounce-slow">🛠️</span>
          <span class="font-semibold">Technical Expertise</span>
        </div>
        <h2 class="text-5xl font-extrabold text-slate-900 dark:text-white mb-6 leading-tight">
          Skills & <span class="bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600 bg-clip-text text-transparent animate-gradient-x">Technologies</span>
        </h2>
        <p class="text-xl md:text-2xl text-slate-600 dark:text-slate-400 max-w-3xl mx-auto leading-relaxed">
          Modern tech stack across frontend, backend, DevOps, and emerging technologies
        </p>
      </div>

      <!-- Skills Grid with Stagger Animation -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8 mb-16 md:mb-24">
        <div
          v-for="(skillGroup, index) in skillGroups"
          :key="skillGroup.category"
          class="group relative bg-white/80 dark:bg-slate-800/80 backdrop-blur-md rounded-3xl p-8 border border-slate-200/50 dark:border-slate-700/50 hover:border-transparent hover:shadow-2xl hover:scale-105 transition-all duration-500 cursor-pointer animate-fade-in-up"
          :class="{ 'ring-4 ring-blue-500/50 scale-105': activeCategory === skillGroup.category }"
          :style="{ animationDelay: `${index * 100}ms` }"
          @click="toggleCategory(skillGroup.category)"
        >
          <!-- Gradient overlay on hover -->
          <div :class="`absolute inset-0 rounded-3xl bg-gradient-to-br ${skillGroup.color} opacity-0 group-hover:opacity-10 transition-opacity duration-500`"></div>
          
          <!-- Animated corner accent -->
          <div class="absolute -top-1 -right-1 w-24 h-24 bg-gradient-to-br from-blue-400/30 to-purple-400/30 dark:from-blue-500/20 dark:to-purple-500/20 rounded-full blur-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <!-- Category header -->
            <div class="flex items-center gap-4 mb-6">
              <div 
                :class="`w-16 h-16 rounded-2xl bg-gradient-to-br ${skillGroup.color} flex items-center justify-center text-3xl shadow-lg group-hover:scale-110 group-hover:rotate-12 transition-all duration-500`"
              >
                {{ skillGroup.icon }}
              </div>
              <h3 class="text-2xl font-bold text-slate-900 dark:text-white group-hover:text-transparent group-hover:bg-gradient-to-r group-hover:from-blue-600 group-hover:to-purple-600 group-hover:bg-clip-text transition-all duration-300">
                {{ skillGroup.category }}
              </h3>
            </div>

            <!-- Skills list with individual animations -->
            <div class="space-y-3 mb-6">
              <div 
                v-for="(skill, skillIndex) in skillGroup.skills" 
                :key="skill" 
                class="group/skill flex items-center gap-3 p-2 rounded-lg hover:bg-slate-50/80 dark:hover:bg-slate-700/50 transition-all duration-300"
                :class="{ 'animate-slide-in-right': activeCategory === skillGroup.category }"
                :style="{ animationDelay: `${skillIndex * 50}ms` }"
              >
                <div class="w-2 h-2 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 group-hover/skill:scale-150 group-hover/skill:shadow-lg transition-all duration-300"></div>
                <span class="text-slate-700 dark:text-slate-300 font-medium group-hover/skill:text-blue-600 dark:group-hover/skill:text-blue-400 group-hover/skill:translate-x-2 transition-all duration-300">
                  {{ skill }}
                </span>
              </div>
            </div>

            <!-- Animated Proficiency bar -->
            <div class="pt-6 border-t border-slate-200/50 dark:border-slate-700/50">
              <div class="flex items-center justify-between mb-3">
                <span class="text-xs text-slate-600 dark:text-slate-400 font-semibold uppercase tracking-wider">Proficiency</span>
                <span class="text-lg font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
                  {{ skillGroup.proficiency }}%
                </span>
              </div>
              <div class="relative h-3 bg-slate-200/50 dark:bg-slate-700/50 rounded-full overflow-hidden">
                <div 
                  :class="`absolute inset-y-0 left-0 bg-gradient-to-r ${skillGroup.color} rounded-full transition-all duration-1000 ease-out shadow-lg`"
                  :style="{ 
                    width: (activeCategory === skillGroup.category || scrollProgress > 0.3) ? `${skillGroup.proficiency}%` : '0%'
                  }"
                ></div>
                <!-- Shimmer effect -->
                <div 
                  class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent animate-shimmer"
                  :style="{ 
                    width: (activeCategory === skillGroup.category || scrollProgress > 0.3) ? `${skillGroup.proficiency}%` : '0%'
                  }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Technical Highlights with Hover Effects -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-16 md:mb-24">
        <div 
          v-for="(highlight, index) in highlights" 
          :key="highlight.label"
          class="group text-center bg-white/80 dark:bg-slate-800/80 backdrop-blur-md rounded-2xl p-8 border border-slate-200/50 dark:border-slate-700/50 hover:border-transparent hover:shadow-2xl hover:scale-110 transition-all duration-500 cursor-pointer animate-fade-in-up"
          :style="{ animationDelay: `${400 + index * 100}ms` }"
        >
          <div :class="`text-5xl mb-4 group-hover:scale-125 group-hover:rotate-12 transition-all duration-500 filter group-hover:drop-shadow-lg`">
            {{ highlight.icon }}
          </div>
          <div :class="`font-bold text-lg text-slate-900 dark:text-white mb-2 group-hover:bg-gradient-to-r ${highlight.gradient} group-hover:bg-clip-text group-hover:text-transparent transition-all duration-300`">
            {{ highlight.label }}
          </div>
          <div class="text-sm text-slate-600 dark:text-slate-400">{{ highlight.detail }}</div>
        </div>
      </div>

      <!-- Tools & Platforms -->
      <div class="bg-white/80 dark:bg-slate-800/80 backdrop-blur-md rounded-3xl p-8 md:p-12 border border-slate-200/50 dark:border-slate-700/50 mb-16 md:mb-24 shadow-xl animate-fade-in-up" style="animation-delay: 800ms">
        <div class="text-center mb-10">
          <h3 class="text-3xl md:text-4xl font-bold text-slate-900 dark:text-white mb-3">
            Tools & <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Platforms</span>
          </h3>
          <p class="text-lg text-slate-600 dark:text-slate-400">
            Technologies I work with daily
          </p>
        </div>

        <!-- Tools grid with stagger animation -->
        <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-4">
          <div 
            v-for="(tool, index) in tools" 
            :key="tool.name"
            class="group relative bg-slate-50/80 dark:bg-slate-900/80 backdrop-blur-sm rounded-2xl p-6 hover:bg-gradient-to-br hover:from-blue-50 hover:to-purple-50 dark:hover:from-blue-900/20 dark:hover:to-purple-900/20 border border-slate-200/50 dark:border-slate-700/50 hover:border-blue-300/50 dark:hover:border-blue-600/50 hover:shadow-xl hover:scale-110 transition-all duration-500 cursor-pointer animate-scale-in"
            :style="{ animationDelay: `${900 + index * 50}ms` }"
            :title="tool.name"
          >
            <div class="flex flex-col items-center gap-3">
              <div class="text-4xl group-hover:scale-125 group-hover:rotate-12 transition-all duration-500 filter group-hover:drop-shadow-lg">
                {{ tool.icon }}
              </div>
              <div class="text-xs font-semibold text-slate-700 dark:text-slate-300 text-center group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors duration-300">
                {{ tool.name }}
              </div>
            </div>
            <!-- Hover glow effect -->
            <div class="absolute inset-0 rounded-2xl bg-gradient-to-br from-blue-400/20 to-purple-400/20 opacity-0 group-hover:opacity-100 transition-opacity duration-500 blur-xl"></div>
          </div>
        </div>
      </div>

      <!-- Learning & Growth -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        <!-- Currently Learning -->
        <div class="group bg-gradient-to-br from-blue-50/80 to-purple-50/80 dark:from-blue-900/20 dark:to-purple-900/20 backdrop-blur-md rounded-3xl p-8 border border-blue-200/50 dark:border-blue-800/30 shadow-xl hover:shadow-2xl hover:scale-105 transition-all duration-500 animate-fade-in-up" style="animation-delay: 1200ms">
          <div class="flex items-center gap-4 mb-8">
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-600 flex items-center justify-center text-2xl shadow-lg group-hover:scale-110 group-hover:rotate-12 transition-all duration-500">
              📚
            </div>
            <h3 class="text-2xl font-bold text-slate-900 dark:text-white">Currently Learning</h3>
          </div>
          <div class="space-y-4">
            <div 
              v-for="(item, index) in currentlyLearning" 
              :key="item" 
              class="group/item flex items-center gap-4 bg-white/60 dark:bg-slate-800/60 backdrop-blur-sm rounded-xl p-4 hover:bg-white/80 dark:hover:bg-slate-700/80 hover:scale-105 hover:shadow-lg transition-all duration-300 animate-slide-in-right"
              :style="{ animationDelay: `${1300 + index * 100}ms` }"
            >
              <div class="w-3 h-3 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 animate-pulse shadow-lg"></div>
              <span class="text-slate-700 dark:text-slate-300 font-medium group-hover/item:text-blue-600 dark:group-hover/item:text-blue-400 transition-colors">{{ item }}</span>
            </div>
          </div>
        </div>

        <!-- Certifications & Achievements -->
        <div class="group bg-gradient-to-br from-purple-50/80 to-pink-50/80 dark:from-purple-900/20 dark:to-pink-900/20 backdrop-blur-md rounded-3xl p-8 border border-purple-200/50 dark:border-purple-800/30 shadow-xl hover:shadow-2xl hover:scale-105 transition-all duration-500 animate-fade-in-up" style="animation-delay: 1400ms">
          <div class="flex items-center gap-4 mb-8">
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-purple-500 to-pink-600 flex items-center justify-center text-2xl shadow-lg group-hover:scale-110 group-hover:rotate-12 transition-all duration-500">
              🏆
            </div>
            <h3 class="text-2xl font-bold text-slate-900 dark:text-white">Achievements</h3>
          </div>
          <div class="space-y-4">
            <div 
              v-for="(achievement, index) in achievements" 
              :key="achievement" 
              class="group/item flex items-center gap-4 bg-white/60 dark:bg-slate-800/60 backdrop-blur-sm rounded-xl p-4 hover:bg-white/80 dark:hover:bg-slate-700/80 hover:scale-105 hover:shadow-lg transition-all duration-300 animate-slide-in-left"
              :style="{ animationDelay: `${1500 + index * 100}ms` }"
            >
              <div class="w-3 h-3 rounded-full bg-gradient-to-r from-purple-600 to-pink-600 shadow-lg"></div>
              <span class="text-slate-700 dark:text-slate-300 font-medium group-hover/item:text-purple-600 dark:group-hover/item:text-purple-400 transition-colors">{{ achievement }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

interface SkillGroup {
  category: string
  icon: string
  skills: string[]
  proficiency: number
  color: string
}

interface Highlight {
  icon: string
  label: string
  detail: string
  gradient: string
}

interface Tool {
  name: string
  icon: string
}

const activeCategory = ref<string | null>(null)
const scrollProgress = ref(0)

const skillGroups: SkillGroup[] = [
  {
    category: 'Frontend',
    icon: '⚛️',
    skills: ['React.js', 'Vue.js', 'Next.js', 'Nuxt.js', 'TypeScript', 'Tailwind CSS', 'SCSS'],
    proficiency: 95,
    color: 'from-blue-500 to-cyan-500'
  },
  {
    category: 'Backend',
    icon: '⚙️',
    skills: ['Node.js', 'Express.js', 'Nest.js', 'FastAPI', 'Python', 'GraphQL', 'REST APIs'],
    proficiency: 92,
    color: 'from-purple-500 to-pink-500'
  },
  {
    category: 'Databases',
    icon: '🗄️',
    skills: ['MongoDB', 'PostgreSQL', 'Redis', 'Firestore', 'Vector Databases'],
    proficiency: 90,
    color: 'from-emerald-500 to-teal-500'
  },
  {
    category: 'DevOps & Cloud',
    icon: '☁️',
    skills: ['Docker', 'AWS', 'GCP', 'GitHub Actions', 'CI/CD', 'Vercel', 'Netlify'],
    proficiency: 85,
    color: 'from-orange-500 to-amber-500'
  },
  {
    category: 'Testing',
    icon: '✅',
    skills: ['Jest', 'Cypress', 'React Testing Library', 'Unit Testing', 'E2E Testing'],
    proficiency: 88,
    color: 'from-rose-500 to-red-500'
  },
  {
    category: 'AI & Data',
    icon: '🤖',
    skills: ['LangChain', 'LangGraph', 'LlamaIndex', 'Dagster', 'ETL Pipelines'],
    proficiency: 75,
    color: 'from-violet-500 to-indigo-500'
  }
]

const highlights: Highlight[] = [
  { icon: '📱', label: 'Mobile First', detail: 'Responsive Design', gradient: 'from-blue-400 to-cyan-400' },
  { icon: '⚡', label: 'Performance', detail: '95+ Lighthouse', gradient: 'from-yellow-400 to-orange-400' },
  { icon: '🔒', label: 'Security', detail: 'Best Practices', gradient: 'from-green-400 to-emerald-400' },
  { icon: '♿', label: 'Accessibility', detail: 'WCAG Compliant', gradient: 'from-purple-400 to-pink-400' }
]

const tools: Tool[] = [
  { name: 'Git', icon: '🔧' },
  { name: 'VS Code', icon: '💻' },
  { name: 'Figma', icon: '🎨' },
  { name: 'Postman', icon: '📮' },
  { name: 'Jira', icon: '📊' },
  { name: 'Slack', icon: '💬' },
  { name: 'Docker', icon: '🐳' },
  { name: 'Kubernetes', icon: '☸️' },
  { name: 'AWS', icon: '☁️' },
  { name: 'MongoDB', icon: '🍃' },
  { name: 'Redis', icon: '📦' },
  { name: 'Webpack', icon: '📦' }
]

const currentlyLearning = [
  'Advanced System Design',
  'Microservices Architecture',
  'Web3 & Blockchain',
  'Machine Learning Ops'
]

const achievements = [
  '100K+ Users Impacted',
  '50+ Production Deployments',
  'Multiple Industry Experience',
  'Open Source Contributor'
]

const toggleCategory = (category: string) => {
  activeCategory.value = activeCategory.value === category ? null : category
}

const handleScroll = () => {
  const section = document.getElementById('skills')
  if (section) {
    const rect = section.getBoundingClientRect()
    const progress = Math.max(0, Math.min(1, (window.innerHeight - rect.top) / window.innerHeight))
    scrollProgress.value = progress
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  handleScroll()
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
@keyframes float-slow {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(30px, 30px) scale(1.1); }
}

@keyframes float-medium {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(-40px, 20px) scale(1.15); }
}

@keyframes float-fast {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(20px, -30px) scale(1.2); }
}

@keyframes particle {
  0% { transform: translateY(0) scale(0); opacity: 0; }
  50% { opacity: 1; }
  100% { transform: translateY(-100vh) scale(1); opacity: 0; }
}

@keyframes gradient-x {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

@keyframes bounce-slow {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-right {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-in-left {
  from {
    opacity: 0;
    transform: translateX(20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes scale-in {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.animate-float-slow {
  animation: float-slow 6s ease-in-out infinite;
}

.animate-float-medium {
  animation: float-medium 8s ease-in-out infinite;
  animation-delay: 1s;
}

.animate-float-fast {
  animation: float-fast 5s ease-in-out infinite;
  animation-delay: 2s;
}

.animate-particle {
  animation: particle linear infinite;
}

.animate-gradient-x {
  background-size: 200% 200%;
  animation: gradient-x 3s ease infinite;
}

.animate-bounce-slow {
  animation: bounce-slow 2s ease-in-out infinite;
}

.animate-fade-in-up {
  animation: fade-in-up 0.6s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-right {
  animation: slide-in-right 0.4s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-left {
  animation: slide-in-left 0.4s ease-out forwards;
  opacity: 0;
}

.animate-scale-in {
  animation: scale-in 0.4s ease-out forwards;
  opacity: 0;
}

.animate-shimmer {
  animation: shimmer 2s infinite;
}
</style>