<template>
  <div class="example-section">
    <h1>Exemples d’interventions </h1>
    <div class="cards-container">
      <div class="cards-style">
      <BaseCard
          v-for="(card, index) in cards1"
          :key="index"
          :title="card.title"
          :imageSrc="card.imageSrc"
          :imageWidth="imageWidth"
      />
        </div>
<div class="cards-style">
      <BaseCard
          v-for="(card, index) in cards2"
          :key="index"
          :title="card.title"
          :imageSrc="card.imageSrc"
          :imageWidth="imageWidth"
      />
    </div>
    </div>
  </div>
</template>

<style scoped>
h1, h3 {
  font-family: 'Alkatra', sans-serif;
}

.example-section {
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
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}
.cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  transition: transform 0.5s ease;
}
.cards-container:hover{
  transform: scale(1.05);
}
.cards-style {
  border: 1px solid #24424A;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}
</style>

<script setup >
import BaseCard from "~/components/BaseCard.vue";

import maison from "@/assets/images/avant1.jpg";
import appartement from "@/assets/images/apres1.jpg";
import locaux from "@/assets/images/avant2.jpg";
import bureaux from "@/assets/images/apres2.jpg";


const imageWidth = ref('60vh')

const updateImageWidth = () => {
  imageWidth.value = window.innerWidth < 600 ? '40vh' : '60vh'
}

onMounted(() => {
  updateImageWidth()
  window.addEventListener('resize', updateImageWidth)
})

onBeforeUnmount(() => {
  window.removeEventListener('resize', updateImageWidth)
})

const cards1 = [
  { title: 'Avant', imageSrc: maison },
  { title: 'Après', imageSrc: appartement }
]
const cards2 = [
  { title: 'Avant', imageSrc: locaux },
  { title: 'Après', imageSrc: bureaux }
]
</script>