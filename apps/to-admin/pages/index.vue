<template>
    <div>
      <h1>管理者向けページ(pages)</h1>
      <MainVisual />
      <CaseConverter />
      <Footer />
    </div>
  </template>
  
  <script setup>
  import Footer from "@kurukuruz/shared-components/src/components/DefaultFooter.vue"
  
  useHead({
    title: "管理者向け | @kurukuruz/monorepo",
    meta: [
      {
        name: "robots",
        content: "noindex,nofollow"
      }
    ]
  })
  </script>
  