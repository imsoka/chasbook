<script setup lang="ts">
interface Props {
  src: string;
}

const props = defineProps<Props>();
</script>

<template>
  <div class="video">
    <video controls>
        <source :src="src" type="video/mp4">
    </video>
  </div>
</template>

<style lang="scss">
.video {
    max-width: 1280px;
}

@media only screen and (min-width: 768px) {
  .video {
    margin-inline: auto;

    video {
        width: 100%;
    }
  }
}
</style>
