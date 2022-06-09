<script setup lang="ts">
import { RouterView } from "vue-router";
import bg from "@/assets/img/bg/bg.gif";
</script>

<template>
    <div class="root" :style="{ backgroundImage: `url(${bg})` }">
        <RouterView />
    </div>
</template>

<style lang="scss">
.root {
    min-height: 100vh;
}
.hidden {
    display: none;
    opacity: 0;
}
</style>
