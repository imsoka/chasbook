<script setup lang="ts">
    import TheTitle from "@/components/TheTitle.vue";
    import Planet from "@/components/Planet.vue";
    import TheVideo from "@/components/TheVideo.vue";
</script>

<template>
  <header class="header">
    <TheTitle name="HELENA" surnames="LOBERA ARROYO" job="CREATIVA"/>
  </header>
  <main>
    <TheVideo youtube src="https://www.youtube-nocookie.com/embed/LDU_Txk06tM?controls=0"/>
  </main>
  <footer class="footer">
  </footer>
</template>

<style lang="scss">
    .header {
        display: flex;
        justify-content: center;
        height: 20vh;
    }

    .footer {

    }
</style>
