<script setup lang="ts">
import euthanasy from "@/assets/img/planets/euthanasy.png";
import justShare from "@/assets/img/planets/just_share.png";
import meta from "@/assets/img/planets/meta.png";
import psoe from "@/assets/img/planets/psoe.png";
import spotify from "@/assets/img/planets/spotify.png";

interface Props {
  type?: string;
}

const props = defineProps<Props>();
</script>

<template>
  <img class="planet" :src="spotify" />
</template>

<style lang="scss">
.planet {
  position: absolute;
  width: 10rem;
  bottom: 10em;
  right: 0;
}
</style>
