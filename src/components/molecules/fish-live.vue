<template>
    <div class="fish-live" @click="feed">
        <Tooltip content="Feed me!" v-if="showTooltip" />
        <Fish content="https://ik.imagekit.io/zjvju1m8yb/genshin-aquarium/Mask%20group-1_eEXhCkt2C.png?updatedAt=1697060575549" />
        <FishName content="The rock" />
        <FishLife :life="fishLife" />
    </div>
</template>

<script setup>
    import { ref, onMounted, watch, computed } from 'vue'
    import Tooltip from '../atoms/tooltip.vue'
    import Fish from '../atoms/fish.vue'
    import FishName from '../atoms/fish-name.vue' 
    import FishLife from '../atoms/fish-life.vue'

    const fishLife = ref(100)
    const intervalId = ref('')

    const feed = () => fishLife.value = 100
    const kill = () => clearInterval(intervalId.value)

    const showTooltip = computed(() => {
        if(fishLife.value <= 60) return true
        return false
    })

    watch(fishLife, (newLife) => {
        if(newLife === 0) kill
    }) 

    onMounted(() => {
        intervalId.value = setInterval(() => { 
            fishLife.value -= 1
        }, 200);
    })
</script>

<style scoped>
</style>