<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>  
    <h1>Vite + Vue3 Site</h1>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>

  <RouterView />
</template>

<style scoped>
nav {
  background-color: #0e0e0e;
  padding: .5rem 1rem;
  margin-bottom: 1rem;
}
a {
  color: #ccc;
  text-decoration: none;
  font-size: 1.3rem;
  margin-inline: 1.5rem;
}
 
h1 {
color: rgb(108, 217, 108);
}
 
a.router-link-active {
  color: rgb(110, 207, 115);
}
</style>