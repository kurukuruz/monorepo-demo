<template>
    <span class="hambuger" :class="{'open': isOpen}"></span>
</template>

<script setup>
defineProps({
    isOpen: Boolean
})
</script>

<style scoped>
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