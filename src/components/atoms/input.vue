<template>
    <input type="text" placeholder="The rock" class="input">
</template>
  
<script setup>
defineProps({
    value: String
})
</script>
  
<style scoped>
.input {
    width: 100%;
    height: 50px;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 0.5rem;
    outline: none;
    background-color: var(--color-background-mute);

    font-size: 1.2rem;
    font-weight: bold;
    color: var(--color-text);
}
</style>