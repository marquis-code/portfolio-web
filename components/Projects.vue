<template>
  <section id="projects" class="py-24 md:py-32 px-6 relative overflow-hidden">
    <!-- Consistent background gradient -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900"></div>
    
    <div class="max-w-7xl mx-auto relative z-10">
      <!-- Section header -->
      <div class="text-center mb-16 md:mb-20">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-sm text-slate-600 dark:text-slate-400 text-sm font-medium border border-slate-200/50 dark:border-slate-700/50 mb-6">
          <span class="w-2 h-2 rounded-full bg-blue-500 animate-pulse"></span>
          Portfolio
        </div>
        <h2 class="text-5xl font-bold text-slate-900 dark:text-white mb-6">
          Featured <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Projects</span>
        </h2>
        <p class="text-lg md:text-xl text-slate-600 dark:text-slate-400 max-w-2xl mx-auto leading-relaxed">
          Diverse portfolio showcasing expertise across industries and technology stacks
        </p>
      </div>

      <!-- Industry filter tabs -->
      <div class="flex flex-wrap gap-3 justify-center mb-12 md:mb-16">
        <button
          v-for="industry in industries"
          :key="industry"
          @click="activeIndustry = industry"
          :class="[
            'px-5 py-2.5 rounded-full font-medium transition-all duration-300 text-sm',
            activeIndustry === industry
              ? 'bg-gradient-to-r from-blue-600 to-purple-600 text-white shadow-lg scale-105'
              : 'bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm border border-slate-200/50 dark:border-slate-700/50 text-slate-700 dark:text-slate-300 hover:border-blue-300/50 dark:hover:border-blue-700/50 hover:scale-105 hover:shadow-md'
          ]"
        >
          {{ industry }}
        </button>
      </div>

      <!-- Featured Projects Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(project, index) in filteredProjects"
          :key="project.id"
          :class="[
            'group relative bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl overflow-hidden border border-slate-200/50 dark:border-slate-700/50 hover:shadow-xl hover:-translate-y-2 hover:border-blue-200/50 dark:hover:border-blue-700/50 transition-all duration-500',
            index === 0 && activeIndustry === 'All' ? 'md:col-span-2 lg:col-span-2' : ''
          ]"
        >
          <!-- Project gradient header -->
          <div 
            class="relative overflow-hidden"
            :class="index === 0 && activeIndustry === 'All' ? 'h-64' : 'h-48'"
            :style="{ background: `linear-gradient(135deg, ${project.gradient[0]}, ${project.gradient[1]})` }"
          >
            <!-- Animated overlay -->
            <div class="absolute inset-0 bg-gradient-to-br from-white/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <!-- Large decorative icon -->
            <div class="absolute inset-0 flex items-center justify-center">
              <div class="text-white/10 font-bold group-hover:scale-110 transition-transform duration-500" :class="index === 0 && activeIndustry === 'All' ? 'text-9xl' : 'text-8xl'">
                {{ project.icon }}
              </div>
            </div>

            <!-- Industry badge -->
            <div class="absolute top-4 right-4">
              <span class="px-3 py-1.5 rounded-full bg-white/90 dark:bg-slate-900/90 backdrop-blur-sm text-xs font-semibold text-slate-700 dark:text-slate-300 shadow-lg border border-white/20">
                {{ project.industry }}
              </span>
            </div>

            <!-- Year badge -->
            <div class="absolute bottom-4 left-4">
              <span class="px-3 py-1.5 rounded-full bg-white/20 backdrop-blur-md text-xs font-semibold text-white border border-white/30">
                {{ project.year }}
              </span>
            </div>
          </div>

          <!-- Project content -->
          <div class="p-6 md:p-7">
            <h3 class="text-xl md:text-2xl font-bold text-slate-900 dark:text-white mb-3 group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors">
              {{ project.name }}
            </h3>
            <p class="text-slate-600 dark:text-slate-400 text-sm md:text-base leading-relaxed mb-5">
              {{ project.description }}
            </p>

            <!-- Tech stack -->
            <div class="flex flex-wrap gap-2 mb-5">
              <span 
                v-for="tech in project.technologies" 
                :key="tech" 
                class="px-3 py-1.5 rounded-lg bg-slate-100/80 dark:bg-slate-700/80 text-slate-700 dark:text-slate-300 text-xs font-medium hover:bg-blue-100/80 dark:hover:bg-blue-900/30 hover:text-blue-600 dark:hover:text-blue-400 transition-all duration-300"
              >
                {{ tech }}
              </span>
            </div>

            <!-- View project link -->
            <!-- <div class="flex items-center justify-between pt-4 border-t border-slate-200/50 dark:border-slate-700/50">
              <a 
                href="#" 
                class="inline-flex items-center gap-2 text-blue-600 dark:text-blue-400 hover:gap-3 transition-all duration-300 font-semibold text-sm group/link"
              >
                View Project
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </a>
              <div class="flex items-center gap-2">
                <a href="#" class="w-8 h-8 rounded-lg bg-slate-100/80 dark:bg-slate-700/80 flex items-center justify-center hover:bg-blue-100 dark:hover:bg-blue-900/30 transition-colors group/icon">
                  <svg class="w-4 h-4 text-slate-600 dark:text-slate-400 group-hover/icon:text-blue-600 dark:group-hover/icon:text-blue-400" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                  </svg>
                </a>
              </div>
            </div> -->
          </div>
        </div>
      </div>

      <!-- Additional Collections -->
      <div class="mt-16 md:mt-20 space-y-6">
        <!-- Python Projects -->
        <div class="group bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-6 md:p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-lg transition-all duration-300">
          <div class="flex flex-col md:flex-row md:items-center gap-6">
            <div class="flex items-center gap-4 md:w-1/3">
              <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-blue-600 to-purple-600 flex items-center justify-center text-2xl shadow-lg flex-shrink-0">
                🐍
              </div>
              <div>
                <h3 class="text-xl md:text-2xl font-bold text-slate-900 dark:text-white">Python Projects</h3>
                <p class="text-sm text-slate-600 dark:text-slate-400">Data & automation</p>
              </div>
            </div>
            
            <div class="md:w-2/3">
              <p class="text-slate-700 dark:text-slate-300 mb-4 text-sm md:text-base">
                Backend services, data pipelines, and automation tools
              </p>
              <div class="flex flex-wrap gap-2">
                <span v-for="project in pythonProjects" :key="project" class="px-4 py-2 rounded-lg bg-slate-100/80 dark:bg-slate-700/80 text-slate-700 dark:text-slate-300 text-xs md:text-sm font-medium hover:bg-blue-100/80 dark:hover:bg-blue-900/30 hover:scale-105 transition-all duration-300">
                  {{ project }}
                </span>
              </div>
            </div>
          </div>
        </div>

        <!-- TypeScript/Node Projects -->
        <div class="group bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-6 md:p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-lg transition-all duration-300">
          <div class="flex flex-col md:flex-row md:items-center gap-6">
            <div class="flex items-center gap-4 md:w-1/3">
              <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-purple-600 to-pink-600 flex items-center justify-center text-2xl shadow-lg flex-shrink-0">
                ⚡
              </div>
              <div>
                <h3 class="text-xl md:text-2xl font-bold text-slate-900 dark:text-white">TypeScript/Node</h3>
                <p class="text-sm text-slate-600 dark:text-slate-400">Full-stack apps</p>
              </div>
            </div>
            
            <div class="md:w-2/3">
              <p class="text-slate-700 dark:text-slate-300 mb-4 text-sm md:text-base">
                Enterprise applications, microservices, and real-time systems
              </p>
              <div class="flex flex-wrap gap-2">
                <span v-for="project in nodeProjects" :key="project" class="px-4 py-2 rounded-lg bg-slate-100/80 dark:bg-slate-700/80 text-slate-700 dark:text-slate-300 text-xs md:text-sm font-medium hover:bg-purple-100/80 dark:hover:bg-purple-900/30 hover:scale-105 transition-all duration-300">
                  {{ project }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- CTA Section -->
      <div class="mt-16 text-center">
        <div class="inline-block bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-8 md:p-10 border border-slate-200/50 dark:border-slate-700/50 shadow-lg">
          <h3 class="text-2xl md:text-3xl font-bold text-slate-900 dark:text-white mb-4">Want to see more?</h3>
          <p class="text-slate-600 dark:text-slate-400 mb-6 max-w-md mx-auto text-sm md:text-base">
            Check out my GitHub for more projects and open-source contributions
          </p>
          <a href="https://github.com/marquis-code" target="_blank" class="inline-flex items-center gap-3 px-8 py-4 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 text-white font-semibold hover:scale-105 hover:shadow-xl transition-all duration-300 group">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
            Visit GitHub
            <svg class="w-4 h-4 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const activeIndustry = ref('All')

const industries = ['All', 'FinTech', 'EdTech', 'AgroTech', 'InsurTech', 'Mobility', 'Ecommerce']

interface Project {
  id: number
  name: string
  description: string
  industry: string
  technologies: string[]
  gradient: [string, string]
  icon: string
  year: string
}

const projects: Project[] = [
  {
    id: 1,
    name: 'Maplerad Payment Platform',
    description: 'Multi-currency payment interface processing $2M+ monthly transactions with 99.9% uptime and seamless user experience',
    industry: 'FinTech',
    technologies: ['Vue 3', 'TypeScript', 'Node.js', 'MongoDB'],
    gradient: ['#3b82f6', '#1e40af'],
    icon: '💳',
    year: '2025'
  },
  {
    id: 2,
    name: 'LoanIQ Credit Engine',
    description: 'End-to-end loan processing platform handling 10K+ monthly applications with intelligent credit scoring',
    industry: 'FinTech',
    technologies: ['React', 'Node.js', 'RabbitMQ', 'MongoDB'],
    gradient: ['#8b5cf6', '#6d28d9'],
    icon: '📊',
    year: '2024'
  },
  {
    id: 3,
    name: 'Fundall Investment Dashboard',
    description: 'Comprehensive portfolio management system serving 50K+ users with $5M+ in managed investments',
    industry: 'FinTech',
    technologies: ['React', 'Docker', 'MongoDB', 'Express'],
    gradient: ['#06b6d4', '#0891b2'],
    icon: '💰',
    year: '2024'
  },
  {
    id: 4,
    name: 'Edukoya Gamification',
    description: 'Interactive learning platform with gamification features engaging 15K+ active learners',
    industry: 'EdTech',
    technologies: ['React', 'Vue.js', 'Node.js', 'MongoDB'],
    gradient: ['#10b981', '#059669'],
    icon: '🎓',
    year: '2023'
  },
  {
    id: 5,
    name: 'Farmz2U Marketplace',
    description: 'Agricultural e-commerce platform connecting 500+ farmers with consumers, processing 2K+ monthly orders',
    industry: 'AgroTech',
    technologies: ['Next.js', 'Node.js', 'MongoDB', 'Express'],
    gradient: ['#f59e0b', '#d97706'],
    icon: '🌾',
    year: '2021'
  },
  {
    id: 6,
    name: 'Shuttlers Vehicle System',
    description: 'Offline-first PWA for vehicle inspection and fleet management with real-time tracking',
    industry: 'Mobility',
    technologies: ['React', 'Node.js', 'Kafka', 'PWA'],
    gradient: ['#ec4899', '#be185d'],
    icon: '🚗',
    year: '2024'
  },
  {
    id: 7,
    name: 'MyCoverGenius Insurance',
    description: 'Serverless insurance platform with automated workflows and seamless policy management',
    industry: 'InsurTech',
    technologies: ['Nuxt 3', 'AWS Lambda', 'Serverless'],
    gradient: ['#8b5cf6', '#6366f1'],
    icon: '🛡️',
    year: '2022'
  },
  {
    id: 8,
    name: 'Multi-Seller ERP',
    description: 'Enterprise resource planning system for multi-vendor e-commerce with advanced analytics',
    industry: 'Ecommerce',
    technologies: ['Vue', 'TypeScript', 'Node.js', 'PostgreSQL'],
    gradient: ['#3b82f6', '#06b6d4'],
    icon: '🛒',
    year: '2023'
  },
  {
    id: 9,
    name: 'Dream Space PM Tool',
    description: 'Collaborative project management and moodboard platform for creative teams',
    industry: 'Productivity',
    technologies: ['TypeScript', 'React', 'Node.js', 'MongoDB'],
    gradient: ['#f97316', '#ea580c'],
    icon: '✨',
    year: '2023'
  },
    {
    id: 10,
    name: 'BlackCountry Co-Living',
    description: 'Digital platform connecting tenants with affordable shared accommodations, featuring property management and real-time availability',
    industry: 'PropTech',
    technologies: ['Vue.js', 'Nest.js', 'MongoDB', 'Real-time Sync'],
    gradient: ['#0f172a', '#475569'],
    icon: '🏠',
    year: '2024'
  }

]

const pythonProjects = ['E-commerce Tracker', 'SEO Analyzer', 'Pharmacy API', 'Receipt Insight']
const nodeProjects = ['Admin Dashboards', 'E-commerce ERPs', 'Backend APIs', 'Real-time Systems']

const filteredProjects = computed(() => {
  if (activeIndustry.value === 'All') return projects
  return projects.filter(p => p.industry === activeIndustry.value)
})
</script>