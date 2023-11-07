<template>
    <div class="hamburgerWrapper" @click="toggleState">
        <HamburgerIcon :is-open="isOpen" />
    </div>
</template>

<script setup>
const props = defineProps({
    isOpen: Boolean
})
const emit = defineEmits(["'update:isOpen'"])

const toggleState = () => {
    emit('update:isOpen', !props.isOpen)
}
</script>

<style scoped>
.hamburgerWrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: #ffa;
}
</style>