<script setup lang="ts">
  import { RouterLink } from 'vue-router'

  import { ref } from 'vue'

  const isMenuOpen = ref(false)

  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
  }

  const closeMenu = () => {
    isMenuOpen.value = false
  }
</script>

<template>
  <nav class="navbar">
    <div class="container">
      <router-link to="/" class="logo-link" @click="closeMenu">
        <img src="@/assets/logo.png" alt="Logo" class="logo-image" />
        <h2 class="brand-logo">Mazsik<span>Műhely</span></h2>
      </router-link>

      <button
        class="hamburger"
        :class="{ 'is-active': isMenuOpen }"
        @click="toggleMenu"
        aria-label="Toggle menu"
      >
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>

      <div class="nav-links" :class="{ 'is-open': isMenuOpen }">
        <router-link to="/" class="nav-item home-link" @click="closeMenu">
          <i class="pi pi-home"></i>
        </router-link>
        <router-link to="/about" class="nav-item" @click="closeMenu">Rólunk</router-link>
        <router-link to="/service" class="nav-item" @click="closeMenu">Szolgáltatások</router-link>
        <router-link to="/contact" class="nav-item" @click="closeMenu">Kapcsolat</router-link>
      </div>
    </div>
  </nav>
</template>

<style scoped src="@/assets/styles/header.css"></style>
