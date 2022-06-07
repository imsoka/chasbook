<script setup lang="ts">
import earth from "@/assets/img/planets/earth.png";

interface Props {
  type?: string;
}

const props = defineProps<Props>();
</script>

<template>
  <img class="planet" :src="earth" />
</template>

<script lang="ts"></script>

<style lang="scss">
.planet {
  position: absolute;
  width: 10rem;
  bottom: 10em;
  right: 0;
}
</style>
