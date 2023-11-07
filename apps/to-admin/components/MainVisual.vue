<template>
    <div class="mainVisual">
        管理者向けコンテンツ
        <div class="hamburgerWrapper" @click="isOpen = !isOpen">
            <span class="hambuger" :class="{'open': isOpen}"></span>
        </div>
    </div>
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

.hamburgerWrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: #ffa;
}

.hambuger {
    display: block;
    position: relative;
    width: 20px;
    height: 2px;
    background-color: #000;
    transition: all .4s;
}

.hambuger.open {
    background-color: inherit;
}

.hambuger::before, .hambuger::after {
    content: "";
    display: block;
    position: absolute;
    width: 100%;
    height: 2px;
    background-color: #000;
    transition: all .4s;
}

.hambuger::before {
    top: -6px;
}

.hambuger.open::before {
    transform: rotate(45deg);
    top: 0px
}

.hambuger::after {
    bottom: -6px;
}

.hambuger.open::after {
    transform: rotate(-45deg);
    bottom: 0px;
}
</style>