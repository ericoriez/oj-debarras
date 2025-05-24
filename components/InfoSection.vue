<script setup lang="ts">

</script>

<template>
  <div class="intro-container">
    <div class="intro-section">
      <h1>OJ Débarras</h1>
      <h3> Votre partenaire pour un débarras écologique et responsable !</h3>
      <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo" />
      <p>
        Notre priorité est de vous offrir un service fiable, rapide et discret, avec des tarifs compétitifs adaptés à
        vos besoins.
        Nous nous engageons à intervenir efficacement tout en respectant votre intimité, pour un débarras en toute
        confiance.
      </p>
    </div>
    <div class="img-landing-container">
      <img src="@/assets/images/landing-prez-OJ-min.png" alt="img-landing-prez" class="img-landing">
    </div>
    <p> Simplifiez vos débarras, contactez-nous dès aujourd'hui pour un devis gratuit ! </p>
  </div>
</template>

<style scoped>

.logo {
  width: 150px;
  height: 150px;
}

h1, h3 {
  font-family: 'Alkatra', sans-serif;
  margin: 0;
}

.intro-container {
  text-align: center;
  font-family: 'Inter', sans-serif;
  color: #25424C;
  font-size: 24px;
  padding: 1% 5% 1%;
}

.intro-section {
  font-family: 'Inter', sans-serif;
  color: #25424C;
  font-size: 24px;
  background-color: White;
  padding: 2% 20% 1% 20%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;

}

.img-landing {
  width: 50%;
  height: auto;
  margin: 0 5% 2% 5%;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);

}

.img-landing-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

@media (max-width: 900px) {
  .intro-section {
    padding: 5% 5%;
  }
}
</style>