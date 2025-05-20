

<template>
  <div class="example-section">
    <h1>Exemples d’interventions </h1>
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


.example-section {
  font-family: 'Inter', sans-serif;
  background-color: #6DA48F80;
  color: #25424C;
  padding: 5% 5%;
  margin-bottom: 5%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
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

import maison from "@/assets/images/ex-img-1.png";
import appartement from "@/assets/images/ex-img-2.png";
import locaux from "@/assets/images/ex-img-3.png";
import bureaux from "@/assets/images/ex-img-4.png";


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
        { title: 'Bureaux', imageSrc: bureaux }
      ]
    }
  }
}
</script>