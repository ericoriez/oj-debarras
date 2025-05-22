<script setup lang="ts">

</script>

<template>
  <div class="hero-section">
    <img src="@/assets/images/ex-img-1.png" alt="hero-images" class="background-image" />
    <div class="hero-content">
      <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo" />
      <h1>Nos Prestations</h1>
    </div>
  </div>
  <div class="intro-section">
    <h2>Pour quelles interventions ?</h2>
    <p>OJ Débarras : Votre partenaire pour un débarras écologique et responsable !
      <br>Nous vidons maisons, bureaux, garages et greniers, même lors de successions,
      avec un engagement fort pour l’écologie. Recyclage, revalorisation
      et tarifs compétitifs sont au cœur de notre mission : offrir un service rapide, fiable et respectueux de
      l’environnement.
      <br>Simplifiez vos débarras, contactez-nous dès aujourd'hui pour un devis gratuit !</p>
  </div>
</template>

<style scoped>
.hero-section {
  position: relative;
  width: 100%;
  height: 80vh;
  overflow: hidden;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
  margin-top: 2%;
}
.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
  opacity: 0.5;
}

.hero-content {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  height: 100%;
  padding: 5rem;
  overflow-y: auto;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
  gap: 5%;

}

.logo {
  filter: contrast(200%);
}

h1 {
  font-size: 5rem;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

h2 {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

button {
  background-color: #B6D0C5;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  padding: 1rem 2rem;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  border-radius: 5px;
  border: none;
  margin-bottom: 3rem;
}

button:hover {
  background-color: #A0BDAF;
  opacity: 1;
}

.intro-section {
  font-family: 'Inter', sans-serif;
  color: #25424C;
  font-size: 24px;
  background-color: White;
  padding: 5% 20%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

@media (max-width: 768px) {
  .hero-content {
    padding: 2rem;
    gap: 2rem;
  }
  .intro-section {
    padding: 5% 5%;
  }
}
</style>