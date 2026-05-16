<script setup lang="ts">
  // PrimeIcons használata a vizualitáshoz
</script>

<template>
  <main class="contact-page">
    <div class="container">
      <div class="header">
        <span class="label">Kérdése van? Keressen minket!</span>
        <h1>Kapcsolat</h1>
      </div>

      <div class="contact-grid">
        <div class="contact-info">
          <div class="info-card">
            <div class="icon-box">
              <i class="pi pi-map-marker"></i>
            </div>
            <div class="details">
              <h3>Telephelyünk</h3>
              <p>3300 Eger, Egri út 98.</p>
            </div>
          </div>

          <div class="info-card">
            <div class="icon-box">
              <i class="pi pi-phone"></i>
            </div>
            <div class="details">
              <h3>Telefonszám</h3>
              <a href="tel:+36304942395" class="contact-link">+36 30 494 2395</a>
            </div>
          </div>

          <div class="info-card">
            <div class="icon-box">
              <i class="pi pi-clock"></i>
            </div>
            <div class="details">
              <h3>Nyitvatartás</h3>
              <p>Hétfő - Péntek: 08:00 - 17:00</p>
              <p class="small">Szombat - Vasárnap: Zárva</p>
            </div>
          </div>

          <div class="info-card">
            <div class="icon-box">
              <i class="pi pi-envelope"></i>
            </div>
            <div class="details">
              <h3>E-mail cím</h3>
              <p>info@mazsikmuhely.hu</p>
            </div>
          </div>

          <a href="tel:+36301234567" class="cta-call-btn">
            <i class="pi pi-phone"></i>
            Azonnali hívás
          </a>
        </div>

        <div class="map-wrapper">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2673.427678026949!2d20.366149176821963!3d47.928110465720096!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47408dcf55c2ebed%3A0x134be7c19481f8ab!2sMazsik%20M%C5%B1hely!5e0!3m2!1shu!2shu!4v1778912651702!5m2!1shu!2shu"
            width="600"
            height="450"
            style="border: 0"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped src="@/assets/styles/contact.css"></style>
