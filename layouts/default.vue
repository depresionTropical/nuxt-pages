<template>
  <div>
    <Navbar />
    <main class="container p-3 my-5 border rounder shadow">
      <slot />
    </main>
    <Footer />
  </div>
</template>

<script setup>
// import stylesheet from bootstrap
useHead({
  titleTemplate: "%s - Intro Nuxt",
  bodyAttrs: {
    class: "text-center",
  },
  link: [
    {
      rel: "stylesheet",
      href: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css",
      integrity:
        "sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN",
      crossorigin: "anonymous",
    },
  ],
  script : [
    {
      src : "https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
    
      // body : true 
    }
  ]
});
const currentYear = new Date().getFullYear();
</script>
