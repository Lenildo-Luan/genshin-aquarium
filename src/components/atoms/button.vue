<template>
    <button class="atom-button" @click="$emit('action')">{{ props.content }}</button>
</template>
  
<script setup>
    const props = defineProps({
        content: String
    })
</script>
  
<style scoped>
    .atom-button {
        width: 100%;
        height: 50px;
        padding: 0.5rem 1rem;
        border: none;
        border-radius: 0.5rem;
        outline: none;
        background-color: var(--color-text);

        font-size: 1.2rem;
        font-weight: bold;
        color: var(--color-background-mute);

        transition: 200ms;
    }

    .atom-button:hover {
        opacity: 0.6;
    }

    .atom-button:active {
        opacity: 0.3;
    }
</style>