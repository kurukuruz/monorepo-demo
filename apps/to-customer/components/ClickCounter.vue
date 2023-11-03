<template>
    <div class="buttonContainer">
        <button @click="countUp">CLICK: {{ count }}</button>
    </div>
</template>

<script setup>
const count = ref(0)

const countUp = () => {
    count.value++
}
</script>

<style scoped>
.buttonContainer {
    text-align: center;
}
</style>