<template>
  <div class="service-section">
    <h1>Nos Services</h1>
    <div class="service-text-container">
      <p>
        Nous intervenons pour vider maisons, bureaux, garages et greniers dans de nombreuses situations : un
        déménagement, une succession, une rénovation, la migration de locaux, une faillite ou tout changement important
        dans votre vie.
        À chaque étape, nous agissons avec un engagement fort en faveur de l’écologie, en privilégiant le recyclage et
        la revalorisation des biens.
      </p>
    </div>
    <div class="cards-container">
      <BaseCard
          v-for="(card, index) in cards"
          :key="index"
          :title="card.title"
          :imageSrc="card.imageSrc"
          :imageWidth="imageWidth"
      />
    </div>

  </div>
</template>

<style scoped>
h1, h3 {
  font-family: 'Alkatra', sans-serif;
}
.service-text-container {
  width: 80%;
}

.service-section {
  font-family: 'Inter', sans-serif;
  background-color: #6DA48F80;
  color: #25424C;
  font-size: 24px;
  padding: 1% 5%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

@media (max-width: 450px) {
.service-section {
    padding: 1% 1%;
  gap: 0.5rem;
  }
}
</style>

<script>
import BaseCard from "~/components/BaseCard.vue";

import maison from "@/assets/images/maison.png";
import appartement from "@/assets/images/appartement.png";
import locaux from "@/assets/images/locaux.png";
import bureaux from "@/assets/images/bureaux.png";
import entrepots from "@/assets/images/entrepots.png";

export default {
  components: {
    BaseCard
  },
  data() {
    return {
      imageWidth: '250px',
      cards: [
        {title: 'Maison', imageSrc: maison},
        {title: 'Appartement', imageSrc: appartement},
        {title: 'Locaux Commerciaux', imageSrc: locaux},
        {title: 'Bureaux', imageSrc: bureaux},
        {title: 'Entrepot/Usine', imageSrc: entrepots}
      ]
    }
  }
}
</script>