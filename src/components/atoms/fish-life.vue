<template>
    <progress class="fish-life" :value="life" max="100"></progress>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
    life: Number
})

const fishLifeColor = computed(() => {
    if(props.life <= 30) return 'red'
    else if(props.life <= 60) return 'orange'
    return 'green'
})
</script>

<style scoped> 
    .fish-life {
        background-color: var(--color-background);
        transform: translateY(-1.35rem);
        height: 0.5rem;
        width: 100px;
    }
    
    .fish-life::-webkit-progress-bar {
        background-color: var(--color-background);
    }
    
    .fish-life::-webkit-progress-value {
        background-color:  v-bind(fishLifeColor);
    }
</style>