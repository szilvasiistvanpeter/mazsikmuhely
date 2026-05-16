<script setup lang="ts"></script>

<template>
  <main class="about-page">
    <div class="container">
      <section class="intro-section">
        <div class="text-content">
          <span class="label">Családi vállalkozás évtizedek óta</span>
          <h1>Mazsik Műhely</h1>
          <div class="description">
            <p class="highlight">
              A Mazsik Műhely Heves megyében egyedüli egyéni vállalkozásként kínál speciális fék- és
              kuplung felújítási szolgáltatásokat.
            </p>
            <p>
              Vállalkozásunk alapköve a több évtizedes szakmai tapasztalat és a precizitás. A
              családi tradíciót
              <strong>Mazsik Gábor</strong> viszi tovább, aki 15 évvel ezelőtt vette át a műhely
              vezetését, megőrizve a klasszikus mesterfogásokat, miközben folyamatosan alkalmazkodik
              a modern gépjárműtechnológia elvárásaihoz.
            </p>
          </div>
        </div>
        <div class="image-wrapper">
          <div class="experience-card">
            <span class="number">15+</span>
            <span class="text">év szakmai tapasztalat a vezetésben</span>
          </div>
          <div class="placeholder-img">
            <!-- <img src="@/assets/muhely.jpg" alt="Mazsik Műhely" /> -->
          </div>
        </div>
      </section>

      <section class="activities-section">
        <div class="section-title">
          <h2>Fő tevékenységeink</h2>
          <p>Személy- és teherautók részére egyaránt</p>
        </div>

        <div class="activities-grid">
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Fékdob szabályozás</span>
          </div>
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Féktárcsa szabályozás</span>
          </div>
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Fékpofa betétezés</span>
          </div>
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Kuplung tárcsa betétezés</span>
          </div>
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Kuplungszerkezet köszörülés</span>
          </div>
          <div class="activity-item">
            <i class="pi pi-check-circle"></i>
            <span>Lendkerék szabályozás</span>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<style scoped>
  .about-page {
    background-color: var(--mazsik-black, #0d0d0d);
    color: white;
    padding: 4rem 0;
    min-height: 100vh;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  /* Intro Section */
  .intro-section {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 4rem;
    align-items: center;
    margin-bottom: 6rem;
  }

  .label {
    color: var(--mazsik-red, #e21b22);
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 700;
    font-size: 0.9rem;
    display: block;
    margin-bottom: 1rem;
  }

  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(3rem, 6vw, 4.5rem);
    line-height: 0.9;
    margin-bottom: 2rem;
  }

  .description p {
    line-height: 1.6;
    color: #ccc;
    margin-bottom: 1.5rem;
    font-size: 1.1rem;
  }

  .highlight {
    color: white !important;
    font-size: 1.3rem !important;
    font-weight: 500;
    border-left: 4px solid var(--mazsik-red);
    padding-left: 1.5rem;
  }

  /* Kép és jelvény */
  .image-wrapper {
    position: relative;
  }

  .placeholder-img {
    width: 100%;
    height: 400px;
    background: url('@/assets/muhely.jpg') center/cover no-repeat;
    border: 1px solid #333;
  }

  .experience-card {
    position: absolute;
    bottom: -20px;
    left: -20px;
    background-color: var(--mazsik-red);
    padding: 1.5rem;
    z-index: 10;
    box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.5);
    text-align: center;
    min-width: 150px;
  }

  .experience-card .number {
    display: block;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 3rem;
    line-height: 1;
  }

  .experience-card .text {
    font-size: 0.7rem;
    text-transform: uppercase;
    font-weight: bold;
  }

  /* Tevékenységek */
  .section-title {
    text-align: center;
    margin-bottom: 3rem;
  }

  .section-title h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 3rem;
    margin-bottom: 0.5rem;
  }

  .section-title p {
    color: var(--mazsik-red);
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: 1px;
  }

  .activities-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
  }

  .activity-item {
    background-color: #151515;
    padding: 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    border: 1px solid #222;
    transition: all 0.3s ease;
  }

  .activity-item i {
    color: var(--mazsik-red);
    font-size: 1.2rem;
  }

  .activity-item span {
    text-transform: uppercase;
    font-weight: 600;
    letter-spacing: 0.5px;
  }

  .activity-item:hover {
    background-color: #1a1a1a;
    border-color: var(--mazsik-red);
    transform: scale(1.02);
  }

  /* Responsive */
  @media (max-width: 900px) {
    .intro-section {
      grid-template-columns: 1fr;
      text-align: center;
    }

    .highlight {
      border-left: none;
      border-top: 2px solid var(--mazsik-red);
      padding-left: 0;
      padding-top: 1rem;
    }

    .image-wrapper {
      max-width: 400px;
      margin: 0 auto;
    }
  }
</style>
