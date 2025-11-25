<template>
 <div>
   <UiToast class="z-[9999999]" />
    <NuxtLayout class="z-10">
      <NuxtPage class="z-10" />
    </NuxtLayout>
 </div>
</template>

<style>
body {
    font-family: 'Roobert PRO', sans-serif;
}
</style>

<script setup lang="ts">

useHead({
  title: "Marquis Abah — Fullstack Engineer",
  meta: [
    { charset: "utf-8" },
    { name: "viewport", content: "width=device-width, initial-scale=1" },
    {
      name: "description",
      content:
        "Fullstack Software Engineer with 5+ years experience building scalable and secure products across FinTech, EdTech, HealthTech, and AgroTech.",
    },
    { name: "format-detection", content: "telephone=no" }
  ],
  link: [
    { rel: "preconnect", href: "https://fonts.googleapis.com" },
    { rel: "preconnect", href: "https://fonts.gstatic.com", crossorigin: "" },
    {
      rel: "icon",
      type: "image/png",
      href: "/favicon.ico"
    }
  ]
})

useSeoMeta({
  title: "Marquis Abah — Fullstack Engineer",
  ogTitle: "Marquis Abah — Fullstack Engineer & Product Builder",
  description:
    "Portfolio of Marquis Abah — a Fullstack Engineer experienced in scalable backend systems, distributed architecture, DevOps, and modern UI engineering.",
  ogDescription:
    "Explore portfolio, experience, projects, and expertise of Marquis Abah — Fullstack Software Engineer building global digital products.",
  ogImage: "/images/portfolio-og.png",
  ogUrl: "https://marquisabah.com",
  twitterTitle: "Marquis Abah — Software Engineer",
  twitterDescription:
    "Fullstack Engineer building scalable and production-ready digital products, microservices, and automated DevOps pipelines.",
  twitterImage: "/images/portfolio-og.png",
  twitterCard: "summary_large_image"
})

</script>
