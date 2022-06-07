<script setup lang="ts">
    interface Props {
        youtube?: boolean,
        src: string,
    };

    const props = defineProps<Props>();
</script>

<template>
    <div class="video">
        <div v-if="youtube" class="video__youtube">
            <iframe
                :src="src"
                frameborder="0"
                allow="
                    accelerometer;
                    autoplay;
                    clipboard-write;
                    encrypted-media;
                    gyroscope;
                    picture-in-picture">
            </iframe>
        </div>
    <video v-else :src="src"></video>
    </div>
</template>

<style lang="scss">
    .video {
        &__youtube {
            position: relative;
            padding-bottom: 56.25%;
            padding-top: 30px;
            height: 0;
            overflow: hidden;

            iframe, object, embed {
                position:absolute;
                top:0;
                left:0;
                width:100%;
                height:100%;
            }
        }
    }

    @media only screen and (min-width: 1280px) {
        .video {
            max-width: 1280px;
            margin-inline: auto;
            margin-block-start: 4rem;
        }
    }
</style>
