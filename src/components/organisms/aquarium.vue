<template>
    <div class="aquarium">
        <FishLive />
    </div>
</template>

<script setup>
    import FishLive from '../molecules/fish-live.vue'
</script>

<style scoped>
    .aquarium {
        flex: 1;
        display: flex;
        align-items: center;
        justify-content: center;
        background-size: cover;
        background-image: url('https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/007bed9a4088edf7855bd68e348dbe98_2520438321202498913_6unxhiuwe.webp?updatedAt=1697060575778');
    }
</style>