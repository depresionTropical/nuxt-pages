<template>
  <div>
    <Navbar />
    <main>
      <slot />
    </main>
    <footer>&copy; Hugo Martínez -{{ currentYear }}</footer>
  </div>
</template>

<script setup>
// import stylesheet from bootstrap
useHead({
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
