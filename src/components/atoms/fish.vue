<template>
    <img :src="content" alt="Fish image" :class="{ selected: selected}">
</template>

<script setup>
    defineProps({
        content: String,
        selected: Boolean
    })
</script>

<style scoped>
    .selected {
        border: 10px solid black;
    }
</style>