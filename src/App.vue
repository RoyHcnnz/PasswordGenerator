<script setup lang="ts">
import Matrix from './components/Matrix.vue';
import HeaderBar from './components/HeaderBar.vue';
import PasswordGenerator from './components/PasswordGenerator.vue';
import FooterBar from './components/FooterBar.vue';
</script>

<template>
  <!-- Matrix / -->
  <header>
    <HeaderBar/>
  </header>
  <PasswordGenerator />

  <FooterBar />
</template>

<style scoped>
</style>
