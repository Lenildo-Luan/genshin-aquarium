<template>
    <div class="fish-name">
        <Text content="The rock" />
    </div>
</template>

<script setup>
import Text from '../atoms/text.vue'
</script>

<style scoped> 
    .fish-name {
        text-align: center;
        border-top-right-radius: 0.5rem;
        border-top-left-radius: 0.5rem;
        padding: 0.2rem;
        /* background-color: var(--color-border); */
        transform: translateY(-0.5rem);

    }
</style>