<script setup lang="ts">
defineProps<{
  title: string;
  subtitle: string;
}>();
</script>

<template>
  <section class="hero-container">
    <div class="hero-wrapper">
      <div class="text-content">
        <h1 class="hero-title">{{ title }}</h1>
        <p class="hero-subtitle">{{ subtitle }}</p>

        <div class="actions">
          <slot name="actions">
            <a href="/service" class="cta-button">Fedezze fel szolgáltatásainkat</a>
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

<style scoped>
.hero-container {
  position: relative;
  width: 100%;
  height: 80vh;
  min-height: 550px;
  background-color: var(--mazsik-black, #0d0d0d);
  display: flex;
  align-items: center;
  overflow: hidden;
}

.hero-wrapper {
  position: relative;
  z-index: 10;
  max-width: 1400px;
  margin: 0 auto;
  width: 100%;
  padding: 0 5%;
}

.text-content {
  max-width: 650px;
}

.hero-title {
  font-family: "Bebas Neue", sans-serif;
  font-size: clamp(2.5rem, 8vw, 4.5rem);
  color: #fff;
  line-height: 0.95;
  margin-bottom: 1.5rem;
  text-transform: uppercase;
}

/* Ha a title prop-ban jön a vörös rész, a szülőben span-nel küldd be, 
   vagy itt stílusozzuk az utolsó szót: */
.hero-title :deep(span) {
  color: var(--mazsik-red, #e21b22);
}

.hero-subtitle {
  font-family: "Montserrat", sans-serif;
  font-size: 1.25rem;
  color: #b0b0b0;
  margin-bottom: 2.5rem;
  max-width: 500px;
  line-height: 1.6;
}

.media-layer {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%; /* A teljes szélességet kitölti, de a gradiens takarja */
  height: 100%;
  z-index: 1;
}

/* Ez biztosítja, hogy a beküldött <img> megfelelően viselkedjen */
.media-layer :deep(img) {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: right center;
}

.gradient-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    90deg,
    rgba(13, 13, 13, 1) 0%,
    rgba(13, 13, 13, 0.85) 30%,
    rgba(13, 13, 13, 0) 70%
  );
  z-index: 5;
}

.cta-button {
  padding: 1rem 2.5rem;
  background-color: var(--mazsik-red, #e21b22);
  color: white;
  text-decoration: none;
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  border: none;
  display: inline-block;
}

.cta-button:hover {
  background-color: #b3151b;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(226, 27, 34, 0.3);
}

@media (max-width: 768px) {
  .gradient-overlay {
    background: rgba(13, 13, 13, 0.7);
  }
  .text-content {
    text-align: center;
    margin: 0 auto;
  }
}
</style>
