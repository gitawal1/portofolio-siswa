<script setup>
import Navbar from "./components/Navbar.vue";
</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <p>Footer</p>
  </footer>
</template>

<style scoped></style>
