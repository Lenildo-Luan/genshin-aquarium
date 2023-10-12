<template>
    <Input @update-name="updateName"/>
    <Button content="Add fish" @click="$emit('addFish', fishName)"/>
</template>

<script setup>
import { ref } from 'vue'
import Input from '../atoms/input.vue'
import Button from '../atoms/button.vue'

const fishName = ref('')

const updateName = (inputValue) => fishName.value = inputValue
</script>

<style scoped>
    .input {
        margin-bottom: 1rem;
    }
</style>