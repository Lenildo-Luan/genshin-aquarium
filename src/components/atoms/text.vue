<template>
    <h2 class="text">{{ props.content }}</h2>
</template>

<script setup>
const props = defineProps({
    content: String
})
</script>

<style scoped>
.text {
    font-size: 1rem;
}
</style>