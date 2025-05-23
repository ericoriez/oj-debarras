<script setup lang="ts">

</script>

<template>
  <div class="contact-container">
    <div class="hero-section">
      <img src="@/assets/images/ex-img-4.png" alt="hero-images" class="background-image"/>
      <div class="hero-content">
        <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo"/>
        <h1>Contact</h1>
      </div>
    </div>

    <div class="intro-section">
      <h2>Zone D'Intervention</h2>
      <p>
        Située au cœur du bassin annécien, nous intervenons dans une large zone allant de l'<strong>Ain</strong> jusqu'à
        <strong>Genève</strong>, en passant
        par toute la <strong>Savoie</strong> et la <strong>Haute-Savoie</strong>.<br>
      </p>
    </div>

    <ContactFormAI/>

    <div class="intro-section">
      <p>
        Qu’il s’agisse d’un <strong>déménagement</strong>, d’une <strong>succession</strong>, d’une
        <strong>rénovation</strong> ou d’un <strong>changement de situation</strong>, nous mettons tout en œuvre pour
        assurer un service <strong>fiable</strong>, aux <strong>tarifs compétitifs</strong> et respectueux de
        l’environnement, grâce au <strong>recyclage</strong> et à la <strong>revalorisation</strong> des biens.<br>
        Contactez-nous dès aujourd’hui pour un <strong>devis gratuit</strong> et simplifiez vos débarras en toute
        sérénité.
      </p>
    </div>
  </div>
  <BaselogoLite/>
</template>

<style scoped>
.hero-section {
  position: relative;
  width: 100%;
  height: 80vh;
  overflow: hidden;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;

  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
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
  gap: 2%;

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
  padding: 1% 20%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.contact-container .intro-section:last-of-type p {
  margin-bottom: 5%;
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

@media (max-width: 425px) {
  h1 {
    font-size: 3rem;
  }
}
.intro-section {
  gap: 0;
}

h2 {
  margin-bottom: 0;
}
</style>