<template>
    <input type="text" :value="value" @input="$emit('updateName', $event.target.value)" class="input" />
</template>
  
<script setup>
defineProps({
    value: String
})
</script>
  
<style scoped>
.input {
    width: 100%;
}
</style>