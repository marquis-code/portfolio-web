<template>
  <section id="about" class="py-24 md:py-32 px-6 relative overflow-hidden">
    <!-- Refined background gradient -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900"></div>
    
    <div class="max-w-7xl mx-auto relative z-10">
      <!-- Section header -->
      <div class="text-center mb-16 md:mb-20">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-sm text-slate-600 dark:text-slate-400 text-sm font-medium border border-slate-200/50 dark:border-slate-700/50 mb-6">
          <span class="w-2 h-2 rounded-full bg-blue-500 animate-pulse"></span>
          About Me
        </div>
        <h2 class="text-5xl font-bold text-slate-900 dark:text-white mb-6">
          From Lab Coat to <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Code</span>
        </h2>
        <p class="text-lg md:text-xl text-slate-600 dark:text-slate-400 max-w-2xl mx-auto leading-relaxed">
          Blending analytical precision from medical science with creative innovation in software engineering
        </p>
      </div>

      <!-- Stats banner - Top -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-6 mb-12">
        <div v-for="(stat, index) in stats" :key="index" class="group relative bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-6 md:p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-lg transition-all duration-300 overflow-hidden">
          <!-- Animated gradient background on hover -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-600/10 to-purple-600/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10 text-center">
            <div class="text-4xl md:text-5xl font-bold mb-2 bg-gradient-to-br from-blue-600 to-purple-600 bg-clip-text text-transparent">
              {{ stat.value }}
            </div>
            <h3 class="font-semibold text-slate-900 dark:text-white mb-1">
              {{ stat.label }}
            </h3>
            <p class="text-xs md:text-sm text-slate-600 dark:text-slate-400">
              {{ stat.description }}
            </p>
            
            <!-- Progress indicator -->
            <div class="mt-4 h-1 bg-slate-200 dark:bg-slate-700 rounded-full overflow-hidden">
              <div 
                class="h-full rounded-full bg-gradient-to-r from-blue-600 to-purple-600 transition-all duration-1000 ease-out group-hover:w-full" 
                :style="{ width: stat.progress }"
              ></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Main content area - Bento grid style -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
        <!-- Large story card - spans 2 columns -->
        <div class="lg:col-span-2 bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-3xl p-8 md:p-10 border border-slate-200/50 dark:border-slate-700/50 shadow-lg hover:shadow-xl transition-all duration-300">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-blue-600 to-purple-600 flex items-center justify-center text-2xl">
              🧬
            </div>
            <h3 class="text-2xl font-bold text-slate-900 dark:text-white">My Journey</h3>
          </div>
          
          <div class="space-y-5 text-slate-700 dark:text-slate-300 leading-relaxed">
            <p class="text-base md:text-lg">
              I create solutions through code. From the meticulous world of medical laboratories to the dynamic realm of software engineering, my journey is a testament to the fusion of science and technology.
            </p>
            
            <p class="text-base">
              As a <span class="font-semibold text-slate-900 dark:text-white">Medical Laboratory Scientist turned Software Engineer</span>, I've dedicated myself to crafting scalable, robust digital products that deliver seamless experiences.
            </p>
            
            <div class="bg-gradient-to-r from-blue-50/50 to-purple-50/50 dark:from-blue-950/30 dark:to-purple-950/30 rounded-xl p-5 border border-blue-100/50 dark:border-blue-800/30">
              <p class="text-sm md:text-base text-slate-700 dark:text-slate-300">
                In my five-year career, I've honed my skills with cutting-edge JavaScript frameworks like <span class="font-semibold text-blue-600 dark:text-blue-400">React</span> and <span class="font-semibold text-purple-600 dark:text-purple-400">Vue</span>, alongside backend development with <span class="font-semibold text-slate-900 dark:text-white">Node.js, Nest.js, Docker, MongoDB</span> and Express.
              </p>
            </div>
            
            <p class="text-base">
              My mission is to transform ideas into impactful realities, ensuring every product is accessible, well-structured, and user-friendly.
            </p>
          </div>
        </div>

        <!-- Tech stack card -->
        <div class="bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-3xl p-8 border border-slate-200/50 dark:border-slate-700/50 shadow-lg hover:shadow-xl transition-all duration-300">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-blue-600 to-purple-600 flex items-center justify-center text-2xl">
              ⚙️
            </div>
            <h3 class="text-xl font-bold text-slate-900 dark:text-white">Tech Stack</h3>
          </div>
          
          <div class="space-y-4">
            <div v-for="(tech, index) in techStack" :key="index" class="group">
              <div class="flex items-center justify-between mb-2">
                <span class="text-sm font-medium text-slate-900 dark:text-white">{{ tech.name }}</span>
                <span class="text-xs text-slate-600 dark:text-slate-400">{{ tech.level }}%</span>
              </div>
              <div class="h-2 bg-slate-200 dark:bg-slate-700 rounded-full overflow-hidden">
                <div 
                  class="h-full rounded-full bg-gradient-to-r from-blue-600 to-purple-600 transition-all duration-1000 group-hover:scale-x-105" 
                  :style="{ width: tech.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Core values - Bottom -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div v-for="(value, index) in coreValues" :key="index" class="group bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-8 border border-slate-200/50 dark:border-slate-700/50 hover:shadow-lg hover:-translate-y-1 transition-all duration-300">
          <div class="flex flex-col items-center text-center">
            <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-600 to-purple-600 flex items-center justify-center text-3xl mb-4 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300">
              {{ value.icon }}
            </div>
            <h3 class="font-bold text-slate-900 dark:text-white mb-3 text-xl">{{ value.title }}</h3>
            <p class="text-sm text-slate-600 dark:text-slate-400 leading-relaxed">{{ value.description }}</p>
          </div>
        </div>
      </div>

      <!-- Download CV button -->
<div class="mt-16 text-center">
  <a
    href="/marquis-resume.pdf"
    download
    class="inline-flex items-center gap-3 px-8 py-4 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 text-white font-semibold hover:shadow-xl hover:scale-105 transition-all duration-300 group"
  >
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
      />
    </svg>
    Download Resume
    <svg
      class="w-4 h-4 group-hover:translate-x-1 transition-transform"
      fill="none"
      stroke="currentColor"
      viewBox="0 0 24 24"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M9 5l7 7-7 7"
      />
    </svg>
  </a>
</div>

    </div>
  </section>
</template>

<script setup lang="ts">
interface Stat {
  value: string
  label: string
  description: string
  progress: string
}

interface CoreValue {
  icon: string
  title: string
  description: string
}

interface TechStack {
  name: string
  level: number
}

const stats: Stat[] = [
  {
    value: '5+',
    label: 'Years Experience',
    description: 'Building scalable products',
    progress: '85%'
  },
  {
    value: '100K+',
    label: 'Users Impacted',
    description: 'Across all projects',
    progress: '92%'
  },
  {
    value: '50+',
    label: 'Projects Shipped',
    description: 'Production ready solutions',
    progress: '88%'
  }
]

const coreValues: CoreValue[] = [
  {
    icon: '🎯',
    title: 'Precision',
    description: 'Attention to detail in every line of code, ensuring quality and reliability'
  },
  {
    icon: '🚀',
    title: 'Innovation',
    description: 'Pushing boundaries with modern tech and creative problem-solving'
  },
  {
    icon: '💡',
    title: 'Impact',
    description: 'Building solutions that matter and make a real difference'
  }
]

const techStack: TechStack[] = [
  { name: 'React & Vue', level: 90 },
  { name: 'Node.js & Nest.js', level: 85 },
  { name: 'TypeScript', level: 88 },
  { name: 'Docker & MongoDB', level: 82 },
  { name: 'UI/UX Design', level: 80 }
]
</script>