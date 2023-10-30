<template>
    <div class="fish-shop">   
        <Text content="Fish type" />
        <FishType />

        <Text content="Fish name" />
        <FishName />
    </div>
</template>

<script setup>
    import FishType from '../molecules/fish-type.vue'
    import FishName from '../molecules/fish-name.vue'
    import Text from '../atoms/text.vue'
</script>

<style scoped>
    .fish-shop {
        width: 19rem;
        padding: 1rem 2rem 1rem 1rem;
        background-color: var(--color-background);
    }

    .fish-shop > .fish-type {
        margin-bottom: 4rem;
    }

    .fish-shop > .text {
        margin-bottom: 1rem;
    }
</style>