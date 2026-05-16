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

<style scoped>
  .contact-page {
    background-color: var(--mazsik-black, #0d0d0d);
    color: white;
    padding: 6rem 0;
    min-height: 100vh;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .header {
    margin-bottom: 4rem;
  }

  .label {
    color: var(--mazsik-red, #e21b22);
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
    font-size: 0.9rem;
  }

  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 4rem;
    margin-top: 0.5rem;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 4rem;
    align-items: start;
  }

  /* Információs kártyák */
  .contact-info {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .info-card {
    background: #151515;
    padding: 1.5rem;
    display: flex;
    gap: 1.5rem;
    align-items: center;
    border: 1px solid #222;
    transition: border-color 0.3s;
  }

  .info-card:hover {
    border-color: var(--mazsik-red);
  }

  .icon-box {
    background: rgba(226, 27, 34, 0.1);
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 4px;
  }

  .icon-box i {
    color: var(--mazsik-red);
    font-size: 1.5rem;
  }

  .details h3 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.4rem;
    margin-bottom: 0.2rem;
    letter-spacing: 1px;
  }

  .details p,
  .contact-link {
    color: #ccc;
    font-size: 1.1rem;
    text-decoration: none;
  }

  .contact-link:hover {
    color: white;
  }

  .small {
    font-size: 0.85rem !important;
    opacity: 0.7;
  }

  /* Hívás gomb */
  .cta-call-btn {
    background-color: var(--mazsik-red);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding: 1.5rem;
    text-decoration: none;
    font-weight: bold;
    text-transform: uppercase;
    font-size: 1.2rem;
    margin-top: 1rem;
    transition: all 0.3s ease;
    box-shadow: 0 10px 20px rgba(226, 27, 34, 0.2);
  }

  .cta-call-btn:hover {
    background-color: #b3151b;
    transform: translateY(-3px);
  }

  /* Térkép */
  .map-wrapper {
    height: 550px;
    background: #1a1a1a;
    border: 1px solid #333;
    position: sticky;
    top: 100px;
  }

  /* Mobil nézet */
  @media (max-width: 900px) {
    .contact-grid {
      grid-template-columns: 1fr;
    }

    .map-wrapper {
      height: 350px;
      order: -1; /* Mobilon legyen felül a térkép */
    }
  }
</style>
