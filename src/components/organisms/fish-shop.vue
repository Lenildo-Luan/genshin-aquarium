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
        padding: 0.5rem;
        background-color: var(--vt-c-white);
    }
</style>