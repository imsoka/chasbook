<script setup lang="ts">
import standingAstronaut from "@/assets/img/astronaut/standing.png";
import talkingAstronaut from "@/assets/img/astronaut/talking.png";
import Bubble from "@/components/Bubble.vue";
import { reactive, onMounted } from "vue";

const state = reactive({
    talking: false,
});

const emit = defineEmits([
    'astronautTalking',
    'astronautHidden',
    'astronautVisible',
]);

const talk = () => {
    state.talking = true;
    emit('astronautTalking');
};

const show = () => {
    gsap.to(".astronaut", {
        duration: 1,
        ease: "none",
        opacity: 1,
        display: "block",
        y: -10,
    });
    emit('astronautVisible');
}

const hide = () => {
    setTimeout(() => {
        gsap.to(".astronaut", {
            duration: 1,
            ease: "none",
            opacity: 0,
            display: "none",
            y: 100,
        });
    }, 500);
    emit('astronautHidden');
}

onMounted(() => {
    show()

    setTimeout(() => {
        talk();
    }, 1000);
});

</script>

<template>
    <div class="astronaut">
        <img v-if="state.talking" class="talking"  :src="talkingAstronaut"/>
        <img v-else :src="standingAstronaut"/>
        <Bubble class="hidden" @bubble-closed="hide">
              <h1 class="bubble__title">¡Hola! Te estaba esperando.</h1>
              <p class="bubble__message">
                  Soy Helena y voy a ser tu guía en este
                  viaje, pero primero, veamos un vídeo.
              </p>
              <span class="bubble__disclaimer">*Para continuar, cierra el bocadillo</span>
        </Bubble>
    </div>
</template>

<style lang="scss">
    .astronaut {
        position: relative;
        img {
            height: 200px;
        }

        .talking {
            transform: translateX(-12px);
        }
    }
</style>
