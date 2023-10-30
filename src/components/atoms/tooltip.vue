<template>
    <div class="tooltip">
        <Text :content="content" />
        <div class="arrow-down"></div>
    </div>
</template>

<script setup>
import Text from '../atoms/text.vue'

defineProps({
    content: String
})
</script>

<style scoped> 
    .tooltip {
        position: relative;
        text-align: center;
        border-radius: 0.5rem;
        padding: 0.2rem;
        background-color: var(--color-background);
    }

    .tooltip > .arrow-down {
        position: absolute;
        width: 0; 
        height: 0; 
        border-left: 0.5rem solid transparent;
        border-right: 0.5rem solid transparent;
        border-top: 0.5rem solid var(--color-background);
        left: 50%;
        transform: translateY(0.25rem) translateX(-50%);
    }

</style>