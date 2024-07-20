<template>
    <h1>
        CSS Based Transition
    </h1>
    <button @click="Show = !Show">Show / Hide</button>
    <transition name="fade">
        <div v-if="Show">Fade</div>
    </transition>
</template>
<script setup lang="ts">
    import { ref } from "vue"
    const Show = ref()
</script>
<style scoped>
    .fade-enter-active,
    .fade-leave-acitve{
        transition: opacity 1s ease;
    }
    .fade-enter-from,
    .fade-leave-to{
        opacity: 0;
    }
</style>