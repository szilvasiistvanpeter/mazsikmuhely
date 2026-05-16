<script setup lang="ts">
  defineProps<{
    title: string
    subtitle: string
  }>()
</script>

<template>
  <section class="hero-container">
    <div class="hero-wrapper">
      <div class="text-content">
        <h1 class="hero-title">{{ title }}</h1>
        <p class="hero-subtitle">{{ subtitle }}</p>

        <div class="actions">
          <slot name="actions">
            <a href="/mazsikmuhely/service" class="cta-button">Fedezze fel szolgáltatásainkat</a>
          </slot>
        </div>
      </div>
    </div>

    <div class="media-layer">
      <slot name="media" />
    </div>

    <div class="gradient-overlay"></div>
  </section>
</template>

<style scoped src="@/assets/styles/hero.css"></style>
