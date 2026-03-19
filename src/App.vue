<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <!-- // todo: Placeholder links -->
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/workshops">Workshops</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped></style>
