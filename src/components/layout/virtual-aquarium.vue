<template>
    <div class="virtual-aquarium"> 
        <FishShop />
        <Aquarium />
    </div>
</template>

<script setup>
    import FishShop from '../organisms/fish-shop.vue'
    import Aquarium from '../organisms/aquarium.vue'
</script>

<style scoped>
    .virtual-aquarium {
        display: flex;
        min-width: 50rem;
        width: 100vw;
        min-height: 35.5rem;
        height: 100vh;
        /* max-width: 100rem; */
        flex-direction: row;
    }
</style>