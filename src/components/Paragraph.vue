<script setup lang="ts">
interface Props {
  content?: string;
  justify?: boolean;
}

const props = defineProps<Props>();
</script>

<template>
  <p class="paragraph__text" :class="{ justified: justify }">
    {{ content }}
  </p>
</template>

<style lang="scss">
.paragraph__text {
  font-family: "montserrat" !important;
  font-family: inherit;
  margin-inline: auto;
  font-size: 1em;
  line-height: 1.2em;
  font-weight: 300;
}

.justified {
  text-align: justify;
}
</style>
