<template>
    <div class="gridWrapper">
        <div class="inputHolder">
            <input type="text" v-model="inputText">
        </div>
        <div class="textDisplay">
            <span>{{ kebab }}</span>
        </div>
    </div>
</template>

<script setup>
const inputText = ref("")
const kebab = computed(() => {
    return inputText.value.replace(/([a-z0-9])([A-Z])/g, '$1-$2')
        .replace(/\s+/g, '-')
	    .toLowerCase()
		.replace(/-?element/, '');
})
</script>

<style scoped>
.gridWrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.inputHolder {
    text-align: right;
}
</style>