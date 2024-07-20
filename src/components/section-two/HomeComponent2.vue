<template>
    <h1>
        Different Transition CSS Styles
    </h1>
    <button @click="Show = !Show">Fade + Add</button>
    <transition name="fade">
        <div v-if="Show">
            Toggle
        </div>
    </transition>
</template>
<script setup lang="ts">
    import { ref } from "vue"
    const Show = ref()
</script>
<style scoped>
    .fade-enter-active{
        transition: all 0.8s ease;
    }
    .fade-leave-active{
        transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
    }
    .fade-enter-from,
    .fade-leave-to{
        transform: translateX(20px);
        opacity: 0;
    }
</style>