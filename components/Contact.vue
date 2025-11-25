<template>
  <section id="contact" class="py-24 px-4 sm:px-6 lg:px-8 relative overflow-hidden">
    <!-- Background gradient matching your theme -->
    <div class="absolute inset-0 bg-gradient-to-br from-slate-50 via-blue-50/50 to-purple-50/30 dark:from-gray-900 dark:via-slate-900 dark:to-gray-900"></div>
    
    <!-- Subtle accent orbs -->
    <div class="absolute top-1/4 -left-32 w-80 h-80 bg-blue-400/10 dark:bg-blue-500/5 rounded-full blur-3xl"></div>
    <div class="absolute bottom-1/4 -right-32 w-80 h-80 bg-purple-400/10 dark:bg-purple-500/5 rounded-full blur-3xl"></div>

    <div class="max-w-6xl mx-auto relative z-10">
      <!-- Header -->
      <div class="text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/80 dark:bg-slate-800/80 backdrop-blur-sm text-slate-700 dark:text-slate-300 text-sm font-medium border border-slate-200/50 dark:border-slate-700/50 mb-5">
          <span class="text-xl">💬</span>
          <span>Get In Touch</span>
        </div>
        <h2 class="text-4xl sm:text-5xl font-bold text-slate-900 dark:text-white mb-4">
          Let's Build Something <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Amazing</span>
        </h2>
        <p class="text-lg text-slate-600 dark:text-slate-400 max-w-2xl mx-auto">
          Ready to bring your ideas to life? Drop me a message and let's create something extraordinary together.
        </p>
      </div>

      <!-- Contact Cards -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5 mb-14">
        <!-- Email -->
        <a 
          href="mailto:abahmarquis@gmail.com"
          class="group relative bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-7 border border-slate-200/50 dark:border-slate-700/50 hover:bg-white dark:hover:bg-slate-800 hover:shadow-xl hover:shadow-blue-500/10 hover:-translate-y-1 transition-all duration-300"
        >
          <div class="flex flex-col items-center text-center gap-4">
            <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-blue-500 to-blue-600 flex items-center justify-center shadow-lg shadow-blue-500/30 group-hover:scale-110 transition-transform duration-300">
              <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
              </svg>
            </div>
            <div>
              <h3 class="font-semibold text-slate-900 dark:text-white mb-1.5">Email</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors break-all">
                abahmarquis@gmail.com
              </p>
            </div>
          </div>
        </a>

        <!-- LinkedIn -->
        <a 
          href="https://www.linkedin.com/in/marquis-abah-584a12199/" 
          target="_blank"
          rel="noopener noreferrer"
          class="group relative bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-7 border border-slate-200/50 dark:border-slate-700/50 hover:bg-white dark:hover:bg-slate-800 hover:shadow-xl hover:shadow-purple-500/10 hover:-translate-y-1 transition-all duration-300"
        >
          <div class="flex flex-col items-center text-center gap-4">
            <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-purple-500 to-purple-600 flex items-center justify-center shadow-lg shadow-purple-500/30 group-hover:scale-110 transition-transform duration-300">
              <svg class="w-7 h-7 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.722-2.004 1.418-.103.249-.129.597-.129.946v5.441h-3.554s.05-8.736 0-9.646h3.554v1.365c.43-.664 1.199-1.608 2.928-1.608 2.136 0 3.745 1.398 3.745 4.4v5.489zM5.337 8.855c-1.144 0-1.915-.758-1.915-1.705 0-.955.77-1.702 1.915-1.702 1.144 0 1.915.747 1.915 1.702 0 .947-.771 1.705-1.915 1.705zm1.589 11.597H3.75V9.861h3.176v10.591z"/>
              </svg>
            </div>
            <div>
              <h3 class="font-semibold text-slate-900 dark:text-white mb-1.5">LinkedIn</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 group-hover:text-purple-600 dark:group-hover:text-purple-400 transition-colors">
                Connect with me
              </p>
            </div>
          </div>
        </a>

        <!-- Phone -->
        <a 
          href="tel:+2348147626503"
          class="group relative bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm rounded-2xl p-7 border border-slate-200/50 dark:border-slate-700/50 hover:bg-white dark:hover:bg-slate-800 hover:shadow-xl hover:shadow-emerald-500/10 hover:-translate-y-1 transition-all duration-300 sm:col-span-2 lg:col-span-1"
        >
          <div class="flex flex-col items-center text-center gap-4">
            <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-emerald-500 to-emerald-600 flex items-center justify-center shadow-lg shadow-emerald-500/30 group-hover:scale-110 transition-transform duration-300">
              <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
              </svg>
            </div>
            <div>
              <h3 class="font-semibold text-slate-900 dark:text-white mb-1.5">Phone</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 group-hover:text-emerald-600 dark:group-hover:text-emerald-400 transition-colors">
                +234 814 762 6503
              </p>
            </div>
          </div>
        </a>
      </div>

      <!-- CTA Button -->
      <div class="text-center mb-20">
        <a 
          href="mailto:abahmarquis@gmail.com"
          class="inline-flex items-center gap-3 px-8 py-4 rounded-full bg-gradient-to-r from-blue-600 to-purple-600 text-white font-semibold shadow-lg shadow-blue-500/30 hover:shadow-xl hover:shadow-blue-500/40 hover:scale-105 transition-all duration-300 group"
        >
          <span>Start a Conversation</span>
          <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
          </svg>
        </a>
      </div>

      <!-- Footer -->
      <div class="pt-12 border-t border-slate-200/50 dark:border-slate-700/50">
        <div class="flex flex-col sm:flex-row items-center justify-between gap-6">
          <!-- Brand -->
          <div class="flex items-center gap-3">
            <div class="w-9 h-9 bg-gradient-to-br from-blue-600 to-purple-600 rounded-lg flex items-center justify-center shadow-lg">
              <span class="text-white font-bold">M</span>
            </div>
            <span class="font-semibold text-slate-900 dark:text-white">Marquis Abah</span>
          </div>

          <!-- Social Links -->
          <div class="flex items-center gap-4">
            <a href="https://github.com/marquis-code/" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center rounded-lg bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm border border-slate-200/50 dark:border-slate-700/50 text-slate-600 dark:text-slate-400 hover:text-blue-600 dark:hover:text-blue-400 hover:border-blue-300 dark:hover:border-blue-600 hover:shadow-lg transition-all">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="https://www.linkedin.com/in/marquis-abah-584a12199/" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center rounded-lg bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm border border-slate-200/50 dark:border-slate-700/50 text-slate-600 dark:text-slate-400 hover:text-purple-600 dark:hover:text-purple-400 hover:border-purple-300 dark:hover:border-purple-600 hover:shadow-lg transition-all">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.722-2.004 1.418-.103.249-.129.597-.129.946v5.441h-3.554s.05-8.736 0-9.646h3.554v1.365c.43-.664 1.199-1.608 2.928-1.608 2.136 0 3.745 1.398 3.745 4.4v5.489zM5.337 8.855c-1.144 0-1.915-.758-1.915-1.705 0-.955.77-1.702 1.915-1.702 1.144 0 1.915.747 1.915 1.702 0 .947-.771 1.705-1.915 1.705zm1.589 11.597H3.75V9.861h3.176v10.591z"/>
              </svg>
            </a>
            <a href="mailto:abahmarquis@gmail.com" class="w-10 h-10 flex items-center justify-center rounded-lg bg-white/70 dark:bg-slate-800/70 backdrop-blur-sm border border-slate-200/50 dark:border-slate-700/50 text-slate-600 dark:text-slate-400 hover:text-emerald-600 dark:hover:text-emerald-400 hover:border-emerald-300 dark:hover:border-emerald-600 hover:shadow-lg transition-all">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
              </svg>
            </a>
          </div>
        </div>

        <!-- Copyright -->
        <div class="mt-8 text-center">
          <p class="text-sm text-slate-500 dark:text-slate-500">
            © 2025 Marquis Abah — Crafted with passion in Lagos, Nigeria
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// No reactive state needed for this static contact section
</script>