<script setup lang="ts">
    interface Props {
        name: string,
        surnames: string,
        job: string,
        inverted?: boolean,
    }

    const props = defineProps<Props>();
</script>

<template>
    <div class="title">
        <h1 class="title__name" :class="{ inverted: inverted }"> {{name}} </h1>
        <h2 class="title__surname" :class="{ inverted: inverted }"> {{surnames}} </h2>
        <h4 class="title__job" :class="{ inverted: inverted }"> {{job}} </h4>
    </div>
</template>

<script lang="ts">
</script>

<style lang="scss" scoped>
    .title {
        text-align: center;
        color: white;
    }

    .title__name {
        font-size: 4em;
        line-height: 1em;
        vertical-align: bottom;
    }

    .title__surname {
        font-size: 2em;
        margin-block-start: -0.5rem;
    }

    .title__job {
        border-block-start: 1px solid white;
        padding-block-start: 0.5rem;
        font-size: 1.25em;
    }

    .inverted {
        color: black;
        border-color: black;
    }
</style>
