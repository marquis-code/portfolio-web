<template>
  <section class="pt-32 pb-20 px-6 relative overflow-hidden min-h-screen flex items-center">
    <!-- Subtle animated background -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900"></div>
    
    <!-- Floating gradient orbs - very subtle -->
    <div class="absolute top-1/4 left-10 w-96 h-96 bg-blue-500/5 dark:bg-blue-500/10 rounded-full blur-3xl animate-float"></div>
    <div class="absolute bottom-1/4 right-10 w-80 h-80 bg-purple-500/5 dark:bg-purple-500/10 rounded-full blur-3xl animate-float-delayed"></div>

    <div class="max-w-6xl mx-auto relative z-10 w-full">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <!-- Left content - The story begins -->
        <div class="space-y-8">
          <!-- Greeting badge -->
          <div class="opacity-0 animate-fade-in-up">
            <span class="inline-flex items-center gap-2 px-5 py-2.5 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-sm text-slate-700 dark:text-slate-300 text-sm font-medium border border-slate-200 dark:border-slate-700 shadow-sm">
              <span class="relative flex h-2 w-2">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-400 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-2 w-2 bg-blue-500"></span>
              </span>
              Available for new opportunities
            </span>
          </div>
          
          <!-- Main headline - staggered reveal -->
          <div class="space-y-4">
            <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight opacity-0 animate-fade-in-up" style="animation-delay: 0.2s;">
              <span class="block text-slate-900 dark:text-white">Hello, I'm</span>
              <span class="block mt-2 bg-gradient-to-r from-blue-600 via-purple-600 to-blue-600 bg-clip-text text-transparent bg-[length:200%_auto] animate-gradient">
                Marquis Abah
              </span>
            </h1>
            
            <p class="text-xl md:text-2xl text-slate-600 dark:text-slate-400 font-medium opacity-0 animate-fade-in-up" style="animation-delay: 0.4s;">
              Fullstack Engineer
            </p>
          </div>

          <!-- Description with typewriter feel -->
          <p class="text-lg text-slate-600 dark:text-slate-400 leading-relaxed max-w-xl opacity-0 animate-fade-in-up" style="animation-delay: 0.6s;">
            I transform ideas into <span class="text-blue-600 dark:text-blue-400 font-semibold">scalable digital products</span> across FinTech, EdTech, and beyond. With 5+ years of experience, I craft seamless experiences that impact over 100K+ users.
          </p>

          <!-- CTA Buttons -->
          <div class="flex flex-wrap gap-4 opacity-0 animate-fade-in-up" style="animation-delay: 0.8s;">
            <a 
              href="#projects" 
              class="group px-8 py-4 rounded-full bg-slate-900 dark:bg-white text-white dark:text-slate-900 font-semibold hover:scale-105 hover:shadow-xl hover:shadow-blue-500/20 transition-all duration-300 flex items-center gap-2"
            >
              View My Work
              <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
              </svg>
            </a>
            <a 
              href="#contact" 
              class="px-8 py-4 rounded-full bg-white dark:bg-slate-800 text-slate-900 dark:text-white font-semibold border-2 border-slate-200 dark:border-slate-700 hover:border-blue-500 dark:hover:border-blue-400 hover:scale-105 transition-all duration-300"
            >
              Let's Talk
            </a>
          </div>

          <!-- Social proof badges -->
          <div class="flex flex-wrap gap-6 pt-4 opacity-0 animate-fade-in-up" style="animation-delay: 1s;">
            <a href="https://github.com/marquis-code" target="_blank" class="group flex items-center gap-2 text-slate-600 dark:text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors">
              <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-800 flex items-center justify-center group-hover:scale-110 group-hover:bg-slate-900 dark:group-hover:bg-white transition-all duration-300">
                <svg class="w-5 h-5 group-hover:text-white dark:group-hover:text-slate-900" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
              </div>
            </a>
            <a href="https://www.linkedin.com/in/marquis-abah-584a12199/" target="_blank" class="group flex items-center gap-2 text-slate-600 dark:text-slate-400 hover:text-blue-600 dark:hover:text-blue-400 transition-colors">
              <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-800 flex items-center justify-center group-hover:scale-110 group-hover:bg-blue-600 transition-all duration-300">
                <svg class="w-5 h-5 group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.722-2.004 1.418-.103.249-.129.597-.129.946v5.441h-3.554s.05-8.736 0-9.646h3.554v1.365c.43-.664 1.199-1.608 2.928-1.608 2.136 0 3.745 1.398 3.745 4.4v5.489zM5.337 8.855c-1.144 0-1.915-.758-1.915-1.705 0-.955.77-1.702 1.915-1.702 1.144 0 1.915.747 1.915 1.702 0 .947-.771 1.705-1.915 1.705zm1.589 11.597H3.75V9.861h3.176v10.591z"/>
                </svg>
              </div>
            </a>
            <a href="mailto:abahmarquis@gmail.com" class="group flex items-center gap-2 text-slate-600 dark:text-slate-400 hover:text-purple-600 dark:hover:text-purple-400 transition-colors">
              <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-800 flex items-center justify-center group-hover:scale-110 group-hover:bg-purple-600 transition-all duration-300">
                <svg class="w-5 h-5 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
              </div>
            </a>
          </div>
        </div>

        <!-- Right side - Visual element -->
        <div class="hidden lg:flex justify-center items-center opacity-0 animate-fade-in-scale" style="animation-delay: 1.2s;">
          <div class="relative">
            <!-- Main card with code snippet -->
            <div class="relative bg-white dark:bg-slate-800 rounded-2xl shadow-2xl p-8 border border-slate-200 dark:border-slate-700 backdrop-blur-sm hover:scale-105 transition-transform duration-500">
              <!-- Terminal header -->
              <div class="flex items-center gap-2 mb-6 pb-4 border-b border-slate-200 dark:border-slate-700">
                <div class="flex gap-1.5">
                  <div class="w-3 h-3 rounded-full bg-red-500"></div>
                  <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                  <div class="w-3 h-3 rounded-full bg-green-500"></div>
                </div>
                <span class="text-xs text-slate-500 dark:text-slate-400 ml-2">engineer.ts</span>
              </div>
              
              <!-- Code content -->
              <pre class="text-sm font-mono text-slate-800 dark:text-slate-200 leading-relaxed"><code><span class="text-purple-600 dark:text-purple-400">const</span> <span class="text-blue-600 dark:text-blue-400">engineer</span> = {
  <span class="text-slate-600 dark:text-slate-400">name:</span> <span class="text-green-600 dark:text-green-400">'Marquis Abah'</span>,
  <span class="text-slate-600 dark:text-slate-400">role:</span> <span class="text-green-600 dark:text-green-400">'Fullstack Engineer'</span>,
  <span class="text-slate-600 dark:text-slate-400">experience:</span> <span class="text-orange-600 dark:text-orange-400">5+</span> <span class="text-slate-500 dark:text-slate-400">years</span>,
  <span class="text-slate-600 dark:text-slate-400">stack:</span> [
    <span class="text-green-600 dark:text-green-400">'React'</span>, <span class="text-green-600 dark:text-green-400">'Vue'</span>, <span class="text-green-600 dark:text-green-400">'Node.js'</span>
  ],
  <span class="text-slate-600 dark:text-slate-400">passion:</span> <span class="text-green-600 dark:text-green-400">'Building scalable products'</span>
};</code></pre>
            </div>

            <!-- Floating stat cards -->
            <div class="absolute -bottom-6 -right-6 bg-gradient-to-br from-blue-500 to-purple-600 rounded-xl shadow-xl p-4 w-48 animate-float">
              <div class="text-white text-sm font-medium">Impact</div>
              <div class="text-white text-3xl font-bold mt-1">100K+</div>
              <div class="text-blue-100 text-xs mt-1">Users Reached</div>
            </div>

            <div class="absolute -top-6 -left-6 bg-white dark:bg-slate-800 rounded-xl shadow-xl p-4 w-40 border border-slate-200 dark:border-slate-700 animate-float-delayed">
              <div class="text-slate-600 dark:text-slate-400 text-sm font-medium">Experience</div>
              <div class="text-slate-900 dark:text-white text-3xl font-bold mt-1">5+</div>
              <div class="text-slate-500 dark:text-slate-500 text-xs mt-1">Years Building</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Scroll indicator -->
      <!-- <div class="absolute bottom-10 left-1/2 -translate-x-1/2 opacity-0 animate-fade-in-up" style="animation-delay: 1.5s;">
        <div class="flex flex-col items-center gap-2 text-slate-400 dark:text-slate-600">
          <span class="text-xs font-medium">Scroll to explore</span>
          <div class="w-6 h-10 rounded-full border-2 border-slate-300 dark:border-slate-700 flex items-start justify-center p-2">
            <div class="w-1 h-2 bg-slate-400 dark:bg-slate-600 rounded-full animate-bounce"></div>
          </div>
        </div>
      </div> -->
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
@keyframes float {
  0%, 100% {
    transform: translateY(0) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(5deg);
  }
}

@keyframes float-delayed {
  0%, 100% {
    transform: translateY(0) rotate(0deg);
  }
  50% {
    transform: translateY(-25px) rotate(-5deg);
  }
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

@keyframes fade-in-scale {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.animate-float {
  animation: float 8s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 10s ease-in-out infinite;
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
}

.animate-fade-in-scale {
  animation: fade-in-scale 1s ease-out forwards;
}

.animate-gradient {
  animation: gradient 8s linear infinite;
}
</style>