<template>
  <section id="experience" class="py-24 md:py-32 px-6 relative overflow-hidden">
    <!-- Consistent background gradient -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900"></div>
    
    <div class="max-w-7xl mx-auto relative z-10">
      <!-- Section header -->
      <div class="text-center mb-16 md:mb-20">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-sm text-slate-600 dark:text-slate-400 text-sm font-medium border border-slate-200/50 dark:border-slate-700/50 mb-6">
          <span class="w-2 h-2 rounded-full bg-purple-500 animate-pulse"></span>
          Career Journey
        </div>
        <h2 class="text-5xl font-bold text-slate-900 dark:text-white mb-6">
          Work <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Experience</span>
        </h2>
        <p class="text-lg md:text-xl text-slate-600 dark:text-slate-400 max-w-2xl mx-auto leading-relaxed">
          Built impactful products at leading companies across diverse industries
        </p>
      </div>

      <!-- Timeline -->
      <div class="relative">
        <!-- Vertical gradient line -->
        <div class="hidden lg:block absolute left-1/2 top-0 bottom-0 w-0.5 bg-gradient-to-b from-blue-500/50 via-purple-500/50 to-blue-500/50 transform -translate-x-1/2"></div>

        <!-- Experience items -->
        <div class="space-y-8 md:space-y-12">
          <div 
            v-for="(job, index) in experiences" 
            :key="index"
            :class="[
              'relative',
              index % 2 === 0 ? 'lg:pr-[50%] lg:pl-0' : 'lg:pl-[50%] lg:pr-0'
            ]"
          >
            <!-- Timeline dot -->
            <div class="hidden lg:block absolute top-8 left-1/2 transform -translate-x-1/2 z-20">
              <div class="relative">
                <div class="w-5 h-5 rounded-full bg-gradient-to-br from-blue-600 to-purple-600 shadow-lg ring-4 ring-white/80 dark:ring-slate-900/80 backdrop-blur-sm"></div>
                <div class="absolute inset-0 rounded-full bg-gradient-to-br from-blue-500 to-purple-600 animate-ping opacity-20"></div>
              </div>
            </div>

            <!-- Content card -->
            <div :class="[
              'relative',
              index % 2 === 0 ? 'lg:mr-8' : 'lg:ml-8'
            ]">
              <div class="group bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-6 md:p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-xl hover:border-blue-200/50 dark:hover:border-blue-700/50 transition-all duration-300">
                <!-- Gradient overlay on hover -->
                <div class="absolute inset-0 rounded-2xl bg-gradient-to-br from-blue-500/5 to-purple-500/5 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                
                <div class="relative z-10">
                  <!-- Header -->
                  <div class="flex flex-wrap items-start justify-between gap-3 mb-4">
                    <div class="flex-1">
                      <h3 class="text-xl md:text-2xl font-bold text-slate-900 dark:text-white mb-2">
                        {{ job.role }}
                      </h3>
                      <div class="flex flex-wrap items-center gap-2 text-sm">
                        <span class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 text-white font-medium">
                          {{ job.company }}
                        </span>
                        <span class="text-slate-600 dark:text-slate-400">{{ job.industry }}</span>
                      </div>
                    </div>
                    <span class="text-sm text-slate-500 dark:text-slate-500 font-medium whitespace-nowrap px-3 py-1 rounded-lg bg-slate-100/80 dark:bg-slate-700/80">
                      {{ job.period }}
                    </span>
                  </div>
                  
                  <!-- Description -->
                  <p class="text-sm md:text-base text-slate-700 dark:text-slate-300 leading-relaxed mb-5">
                    {{ job.description }}
                  </p>
                  
                  <!-- Impact metrics -->
                  <div v-if="job.metrics && job.metrics.length > 0" class="grid grid-cols-2 md:grid-cols-3 gap-4 mb-5 pb-5 border-b border-slate-200/50 dark:border-slate-700/50">
                    <div v-for="(metric, i) in job.metrics" :key="i" class="text-center">
                      <div class="text-xl md:text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
                        {{ metric.value }}
                      </div>
                      <div class="text-xs text-slate-600 dark:text-slate-400 mt-1">
                        {{ metric.label }}
                      </div>
                    </div>
                  </div>
                  
                  <!-- Technologies -->
                  <div class="flex flex-wrap gap-2">
                    <span 
                      v-for="tech in job.technologies" 
                      :key="tech" 
                      class="px-3 py-1.5 rounded-lg bg-slate-100/80 dark:bg-slate-700/80 text-slate-700 dark:text-slate-300 text-xs font-medium hover:bg-blue-100/80 dark:hover:bg-blue-900/30 hover:text-blue-600 dark:hover:text-blue-400 transition-all duration-300 cursor-default"
                    >
                      {{ tech }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Career highlights -->
      <div class="mt-16 md:mt-20 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div v-for="(highlight, index) in careerHighlights" :key="index" class="group bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-lg hover:-translate-y-1 transition-all duration-300">
          <div class="flex flex-col items-center text-center">
            <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-600 to-purple-600 flex items-center justify-center text-3xl mb-4 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300">
              {{ highlight.icon }}
            </div>
            <div class="text-3xl md:text-4xl font-bold text-slate-900 dark:text-white mb-2">
              {{ highlight.value }}
            </div>
            <div class="text-sm text-slate-600 dark:text-slate-400">
              {{ highlight.label }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Metric {
  value: string
  label: string
}

interface Experience {
  role: string
  company: string
  industry: string
  period: string
  description: string
  technologies: string[]
  metrics?: Metric[]
}

interface CareerHighlight {
  icon: string
  value: string
  label: string
}

const experiences: Experience[] = [
  {
    role: 'Fullstack Engineer',
    company: 'Maplerad',
    industry: 'FinTech',
    period: 'Jan 2025 - Present',
    description: 'Architected multi-currency payment interface processing $2M+ monthly transactions with 99.9% uptime. Reduced customer onboarding from 48 to 6 hours with KYC/AML compliance dashboard.',
    technologies: ['Vue 3', 'TypeScript', 'Node.js', 'MongoDB', 'Express.js', 'Redis'],
    // metrics: [
    //   { value: '$2M+', label: 'Monthly Volume' },
    //   { value: '99.9%', label: 'Uptime' },
    //   { value: '6hrs', label: 'Onboarding' }
    // ]
  },
  {
    role: 'Fullstack Engineer',
    company: 'LoanIQ',
    industry: 'FinTech',
    period: 'Jul 2024 - Dec 2024',
    description: 'Developed end-to-end loan processing platform handling 10K+ monthly applications, reducing approval time from 72 to 24 hours. Built credit scoring engine with event-driven architecture.',
    technologies: ['React', 'Node.js', 'Express.js', 'MongoDB', 'RabbitMQ', 'GraphQL'],
    // metrics: [
    //   { value: '10K+', label: 'Applications' },
    //   { value: '24hrs', label: 'Approval Time' }
    // ]
  },
  {
    role: 'Fullstack Engineer',
    company: 'Fundall',
    industry: 'FinTech',
    period: 'Jan 2024 - Jun 2024',
    description: 'Engineered admin dashboard managing 50K+ users and $5M+ portfolios. Built scalable microservices with Redis caching, integrated 4 investment schemes serving 20K+ investors.',
    technologies: ['React', 'Node.js', 'MongoDB', 'Docker', 'Redis', 'Express.js'],
    // metrics: [
    //   { value: '50K+', label: 'Users' },
    //   { value: '$5M+', label: 'Portfolios' }
    // ]
  },
  {
    role: 'Fullstack Engineer',
    company: 'Shuttlers',
    industry: 'Mobility Tech',
    period: 'Jun 2023 - Mar 2024',
    description: 'Built vehicle inspection platform with offline-first PWA processing 500+ daily inspections. Developed microservices with Kafka event streaming managing 10K+ monthly trips.',
    technologies: ['React', 'Node.js', 'Kafka', 'MongoDB', 'Express.js', 'PWA'],
    // metrics: [
    //   { value: '500+', label: 'Daily Inspections' },
    //   { value: '10K+', label: 'Monthly Trips' }
    // ]
  },
  {
    role: 'Fullstack Engineer',
    company: 'Edukoya',
    industry: 'EdTech',
    period: 'Sep 2022 - Sep 2023',
    description: 'Developed full-stack gamification system serving 15K+ users. Reduced page load time from 4.2s to 2.8s through frontend optimization and backend query improvements.',
    technologies: ['React', 'Node.js', 'Vue.js', 'MongoDB', 'Express.js', 'Webpack'],
    // metrics: [
    //   { value: '15K+', label: 'Active Users' },
    //   { value: '2.8s', label: 'Load Time' }
    // ]
  },
  {
    role: 'Fullstack Engineer',
    company: 'MyCoverGenius',
    industry: 'InsurTech',
    period: 'Apr 2021 - Jun 2022',
    description: 'Architected serverless infrastructure with Nuxt 3 frontend and AWS Lambda backend. Built 3 production applications handling insurance workflows with RESTful APIs.',
    technologies: ['Nuxt 3', 'AWS Lambda', 'Node.js', 'Serverless', 'REST APIs']
  },
  {
    role: 'Fullstack Engineer',
    company: 'Farmz2U',
    industry: 'AgroTech',
    period: 'Jan 2020 - Mar 2021',
    description: 'Developed e-commerce platform connecting 500+ farmers, processing 2K+ monthly transactions. Built inventory management system with real-time tracking and automated pricing.',
    technologies: ['Next.js', 'Node.js', 'MongoDB', 'Express.js', 'React', 'SEO'],
    // metrics: [
    //   { value: '500+', label: 'Farmers' },
    //   { value: '2K+', label: 'Transactions' }
    // ]
  }
]

const careerHighlights: CareerHighlight[] = [
  { icon: '🏢', value: '7+', label: 'Companies' },
  { icon: '🚀', value: '50+', label: 'Projects Delivered' },
  { icon: '🌍', value: '5+', label: 'Industries' }
]
</script>