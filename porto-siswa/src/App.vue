<script setup>
import AltNavbar from "./components/AltNavbar.vue";
</script>

<template>
  <header>
    <AltNavbar />
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <p>Footer</p>
  </footer>
</template>

<style scoped></style>
