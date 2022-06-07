<script setup lang="ts">
interface Props {
  type: string;
}

const props = defineProps<Props>();
</script>

<template>
  <img class="planet" src="img/planets/earth.png" />
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
