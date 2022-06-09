<script setup lang="ts">
import TheTitle from "@/components/TheTitle.vue";
import Planet from "@/components/Planet.vue";
import TheVideo from "@/components/TheVideo.vue";
import Astronaut from "@/components/Astronaut.vue";
import Rocket from "@/components/Rocket.vue";
import Bubble from "@/components/Bubble.vue";
import Index from "@/assets/video/index.mp4";
import { onMounted } from "vue";

const showVideo = () => {
    setTimeout(() => {
        gsap.to(".video", {
            duration: 2,
            ease: "none",
            display: "block",
            opacity: 1,
            y: 0,
        });

        const video = document.querySelector(".video video");
        setTimeout(() => {
            video.play();
        }, 1000);
    }, 1500);
};

</script>

<template>
    <div class="view">
        <header class="header">
          <TheTitle name="HELENA" surnames="LOBERA ARROYO" job="CREATIVA" />
        </header>
        <div class="content">
          <TheVideo class="hidden" :src="Index"/>
          <Astronaut class="hidden" @astronaut-hidden="showVideo()"/>
        </div>
        <footer class="footer"></footer>
    </div>
</template>

<style lang="scss">
.view {
    min-height: 100vh;
    max-width: 1440px;
    margin-inline: auto;
}

.header {
  padding-block-start: 4rem;
  height: 20vh;
  display: flex;
  justify-content: center;
}

.content {
    height:80vh;
    display:grid;
    grid-template-columns: 1fr 66% 1fr;
    align-items: end;
    justify-items: center;
    padding-block: 2rem;
    padding-inline: 2rem;
    position: relative;
}

.video {
    grid-column-start: span 3;
    transform: translateY(-100px);
}

.astronaut {
    grid-column-start: 3;
}

.bubble {

    &__title {
        font-size: 1.5em;
        font-family:'monstserrat';
        color: #000;
        margin-block-end: 1rem;
    }

    p {
        margin-block-end: 0.5rem;
    }

    &__disclaimer {
        font-size: 0.7em;
        color: #000;
        display:block;
        margin-block-start:1em;
        font-family:'monstserrat';
        font-style: italic;
    }
}
</style>
