<template>
    <div  class="fish" :class="{ selected: selected}" :style="{backgroundImage: `url(${content})`}"> </div>
</template>

<script setup>
    defineProps({
        content: String,
        selected: Boolean
    })
</script>

<style scoped>
    .fish {
        box-sizing: border-box;
        height: 6rem;
        width: 100px;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        transition: 200ms;
    }

   .selected {
        -webkit-filter: drop-shadow(0rem 0rem 0.5rem  var(--color-border));
        filter: drop-shadow(0rem 0rem 0.5rem var(--color-border));
    }

    .fish:hover {
        -webkit-filter: drop-shadow(0rem 0rem 0.5rem  var(--color-border-hover));
        filter: drop-shadow(0rem 0rem 0.5rem  var(--color-border-hover));
    }
</style>