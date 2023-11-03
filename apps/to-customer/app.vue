<template>
  <div>
    <h1>お客様向けページ</h1>
    <MainVisual />
    <ClickCounter />
    <Footer />
  </div>
</template>

<script setup>
import Footer from "@kurukuruz/shared-components/src/components/DefaultFooter.vue"

useHead({
  title: "お客様ページ | @kurukuruz/monorepo",
  meta: [
    {
      name: "description",
      content: "monorepoで作成したお客様向けページ"
    },
    {
      name: "keywords",
      content: "kurukuruz,monorepo,demo"
    },
    {
      property: "og:title",
      content: "お客様ページ | @kurukuruz/monorepo"
    }
  ]
})
</script>
