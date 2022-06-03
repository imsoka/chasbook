<script setup lang="ts">
    import TheTitle from "@/components/TheTitle.vue";
    import Planet from "@/components/Planet.vue";
    import Paragraph from "@/components/Paragraph.vue";
</script>

<template>
  <header>
    <TheTitle name="HELENA" surnames="LOBERA ARROYO" job="CREATIVA"/>
  </header>
  <main>
    <section aria-labelledby="introduction" class="content">
        <Paragraph class="content__text"/>
    </section>
  </main>
  <footer>
  </footer>
</template>

<style lang="scss">
    header {
        display: flex;
        justify-content: center;
    }

    .content {
        font-family: "montserrat";
        margin-block-start: 3rem;
        height: 40vh;

        &__text {
            font-family: inherit;
            margin-inline: auto;
            text-align: justify;
            font-size: 1em;
            line-height: 1.2em;
            font-weight: 300;
            max-width: 80%;
        }
    }
    .planet {
    }
</style>
