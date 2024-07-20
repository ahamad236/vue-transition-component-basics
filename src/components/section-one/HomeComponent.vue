<template>
    <h1>
        Home Component
    </h1>
    <button @click="Show = !Show">Show / Hide</button>
    <transition>
        <div v-if="Show" class="toggle">
            Toggle
        </div>
    </transition>
</template>
<script setup lang=ts>
    import { ref } from "vue"

    const Show = ref()
</script>
<style scoped>
    .toggle{
        margin: 30px;
    }
    .v-enter-active,
    .v-leave-active{
        transition: opacity 1s ease;
    }
    .v-enter-from,
    .v-leave-to{
        opacity: 0;
    }
</style>