<script setup lang="ts">
  defineProps<{
    title: string
    description: string
    iconPath: string
  }>()
</script>

<template>
  <div class="service-card">
    <div class="icon-container">
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path :d="iconPath" />
      </svg>
    </div>
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <div class="accent-bar"></div>
  </div>
</template>
<style scoped src="@/assets/styles/service-card.css"></style>
