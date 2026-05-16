<script setup lang="ts">
  import ServiceCard from './ServiceCard.vue'

  const services = [
    {
      id: 1,
      title: 'Fékrendszer Szerviz',
      description:
        'Teljes körű diagnosztika, fékbetét és féktárcsa csere, fékfolyadék ellenőrzés prémium alkatrészekkel.',
      icon: 'M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22ZM12 18C15.3137 18 18 15.3137 18 12C18 8.68629 15.3137 6 12 6C8.68629 6 6 8.68629 6 12C6 15.3137 8.68629 18 12 18Z',
    },
    {
      id: 2,
      title: 'Alkatrész Kereskedelem',
      description:
        'Gyári és tuning fékalkatrészek beszerzése rövid határidővel, garanciával, közvetlenül a gyártótól.',
      icon: 'M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z',
    },
    {
      id: 3,
      title: 'Versenyfelkészítés',
      description:
        'Extrém igénybevételre tervezett fékrendszerek építése és optimalizálása pályanapokra és versenyekre.',
      icon: 'M13 2L3 14h9l-1 8 10-12h-9l1-8z',
    },
    {
      id: 4,
      title: 'Állapotfelmérés',
      description:
        'Műszeres fékhatás mérés és vizuális ellenőrzés, hogy biztonságban tudhasd magad az utakon.',
      icon: 'M22 12h-4l-3 9L9 3l-3 9H2',
    },
  ]
</script>

<template>
  <section id="szolgaltatasok" class="services-section">
    <div class="container">
      <div class="section-header">
        <h2 class="outline-text">Miben segítünk?</h2>
        <p>Profi megoldások, hogy minden helyzetben meg tudj állni.</p>
      </div>

      <div class="services-grid">
        <ServiceCard
          v-for="service in services"
          :key="service.id"
          :title="service.title"
          :description="service.description"
          :iconPath="service.icon"
        />
      </div>
    </div>
  </section>
</template>

<style scoped src="@/assets/styles/service.css"></style>
