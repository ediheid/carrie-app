<template>
  <main>
    <div class="balloon-wrapper">
      <img src="../assets/images/balloon.png" class="balloon" />
      <SvgLoader name="logos/logo" class="logo" />
    </div>
  </main>
</template>

<script setup lang="ts">
import SvgLoader from '../components/ui/SvgLoader.vue'
</script>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.balloon-wrapper {
  position: relative;
  display: inline-block;
}

.balloon {
  display: block;
  width: auto;
  max-width: 90vw;
  max-height: 90vh;
  height: auto;
}

.logo {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  height: auto;
}

/* // todo: look into responsivity with Carrie */
@media (max-width: 480px) {
  .logo {
    width: 90%;
    top: 5%;
  }
}
</style>
