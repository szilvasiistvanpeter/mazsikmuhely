<script setup lang="ts">
  import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="navbar">
    <div class="container">
      <div class="logo">
        <RouterLink to="/" class="logo-link">
          <img src="@/assets/logo.png" alt="Mazsik Műhely logó" class="logo-image" />
          <h2 class="brand-logo">Mazsik<span>Műhely</span></h2>
        </RouterLink>
      </div>

      <nav class="nav-links">
        <RouterLink to="/" class="nav-item home-link">
          <i class="pi pi-home"></i>
        </RouterLink>
        <RouterLink to="/about" class="nav-item">Rólunk</RouterLink>
        <RouterLink to="/service" class="nav-item">Szolgáltatások</RouterLink>
        <RouterLink to="/contact" class="nav-item">Kapcsolat</RouterLink>
      </nav>
    </div>
  </header>
</template>

<style scoped src="@/assets/styles/header.css"></style>
