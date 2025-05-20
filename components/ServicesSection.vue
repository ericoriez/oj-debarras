

<template>
  <div class="service-section">
    <h1>Nos Services</h1>
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


.service-section {
  font-family: 'Inter', sans-serif;
  background-color: #6DA48F80;
  color: #25424C;
  padding: 5% 5%;
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
</style>

<script >
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
        { title: 'Maison', imageSrc: maison },
        { title: 'Appartement', imageSrc: appartement },
        { title: 'Locaux Commerciaux', imageSrc: locaux },
        { title: 'Bureaux', imageSrc: bureaux },
        { title: 'Entrepot/Usine', imageSrc: entrepots }
      ]
    }
  }
}
</script>