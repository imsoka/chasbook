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

<style lang="scss">
    .title {
        text-align: center;
        color: white;

        &__name {
            font-size: 4em;
            line-height: 1em;
            vertical-align: bottom;
        }

        &__surname {
            font-size: 2em;
            margin-block-start: -0.5rem;
        }

        &__job {
            border-block-start: 1px solid white;
            padding-block-start: 0.5rem;
            font-size: 1.25em;
        }
    }

    .inverted {
        color: black;
        border-color: black;
    }

    @media only screen and (min-width: 1280px) {
        .title__name {
            font-size: 8em;
            line-height: 0.8em;
        }

        .title__surname {
            font-size: 3.7em;
        }

        .title__job {
            font-size: 2em;
        }
    }
</style>
