<template>
    <div class="mainVisual">
        管理者向けコンテンツ
        <HamburgerButton v-model:is-open="isOpen"/>
    </div>
    <span>{{ isOpen }}</span>
</template>

<script setup>
const isOpen = ref(false)
</script>

<style scoped>
.mainVisual {
    height: 10rem;
    background-color: #afa;
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>