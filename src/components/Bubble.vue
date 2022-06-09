<script setup lang="ts">
import { onMounted } from "vue";

const emit = defineEmits([
    'bubbleOpen',
    'bubbleClosed',
]);

/**
 * Hide the bubble
 */
const hide = () => {
    gsap.to(".bubble", {
        duration: 0.5,
        y: 10,
        ease: "none",
        opacity: 0,
        display: "none",
    });
    emit('bubbleClosed');
};

/**
 * Show the bubble
 */
const show = () => {
    gsap.to(".bubble", {
        duration: 0.5,
        y: -10,
        ease: "none",
        opacity: 1,
        display: "block",
    });
    emit('bubbleOpen');
};

onMounted(() => {
    setTimeout(() => {
        show();
    }, 1200);
});

</script>
<template>
    <div class="bubble">
        <div class="bubble__header">
            <svg @click="hide" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="black" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
        </div>
        <div class="bubble__body">
            <slot></slot>
        </div>
    </div>
</template>

<style lang="scss">
    .bubble {
        position: absolute;
        background-color: #fff;
        max-width: 370px;
        border-radius: 0.5rem;
        top:-12rem;
        left: -23rem;

        &__header {
            display: flex;
            padding-inline: 0.5rem;
            padding-block-start: 0.5rem;
            justify-content: end;

            svg {
                cursor: pointer;
                width: 2rem;
            }
        }

        &__body {
            padding-inline: 0.5rem;
            padding-block-end: 0.5rem;
            color: #000;
            font-family: 'montserrat';
            text-align: center;

            p {
                color: #000;
                font-family: 'montserrat';
                margin-block-end: 0.5rem;
            }
        }
    }

    .bubble::before {
        content: "";
        position: absolute;
        width: 0;
        height: 0;
        border-left: 12px solid transparent;
        border-right: 24px solid #fff;
        border-top: 12px solid #fff;
        border-bottom: 20px solid transparent;
        right: 9px;
        bottom: -24px;
    }
</style>
