

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

import maison from "@/assets/images/ex-img-1.png";
import appartement from "@/assets/images/ex-img-2.png";
import locaux from "@/assets/images/ex-img-3.png";
import bureaux from "@/assets/images/ex-img-4.png";


const imageWidth = ref('60vh')

const updateImageWidth = () => {
  imageWidth.value = window.innerWidth < 600 ? '30vh' : '60vh'
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