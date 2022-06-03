<script setup lang="ts">
    interface Props {
        type: string,
    };

    const props = defineProps<Props>();
</script>

<template>
    <img class="planet" src="src/assets/img/planets/earth.png">
</template>

<script lang="ts">
</script>

<style lang="scss">
    .planet {
        width: 150px;
    }
</style>
