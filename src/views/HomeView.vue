<script setup lang="ts">
import TheTitle from "@/components/TheTitle.vue";
import Planet from "@/components/Planet.vue";
import TheVideo from "@/components/TheVideo.vue";
import bg from "@/assets/img/bg/bg.gif";
</script>

<template>
  <div class="view" :style="{ backgroundImage: `url(${bg})` }">
    <header class="header">
      <TheTitle name="HELENA" surnames="LOBERA ARROYO" job="CREATIVA" />
    </header>
    <main class="content">
      <TheVideo
        youtube
        src="https://www.youtube-nocookie.com/embed/LDU_Txk06tM?controls=0"
      />
      <Planet/>
    </main>
    <footer class="footer"></footer>
  </div>
</template>

<style lang="scss">
.view {
    min-height: 100vh;
    padding-block-start: 3em;
}

.header {
  display: flex;
  justify-content: center;
}

.content {
    margin-block-start: 4em;
}

.footer {
}
</style>
