<template>
    <div class="fish-type">
        <Fish v-for="(fish, index) in fishes" :key="fish" :content="fish" @click="selectFish(index)" :selected="index === selectedFish"/>
    </div>
</template>

<script setup>
    import { ref } from 'vue'
    import Fish from '../atoms/fish.vue'

    const selectedFish = ref(0)
    const fishes = ref([
        'https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group-1_eEXhCkt2C.png?updatedAt=1697060575549',
        'https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group-2_oqKPWb6mI.png?updatedAt=1697825476071',
        'https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group-4_Sr4VTTC7D.png?updatedAt=1697060575533',
        'https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group-3_tULLmEc5i.png?updatedAt=1697060575389',
        'https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group_6wv_XAq95.png?updatedAt=1697060575307'
    ])

    const selectFish = (index) => selectedFish.value = index
</script>

<style scoped>
    .fish-type {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 0.5rem;
    }
</style>