<script setup lang="ts">

</script>

<template>
  <div class="eco-section">
    <div class="eco-text">
      <h4>Recyclage et Débarras Éco-Responsable</h4>
      <p>Nous nous engageons à réduire l'impact environnemental en recyclant les matériaux récupérés
        et en favorisant la réutilisation</p>
    </div>
    <div>
      <img src="@/assets/images/eco-img.png" alt="eco-image">
    </div>
  </div>
</template>

<style scoped>
h4 {
  font-family: 'Alkatra', sans-serif;
}


.eco-section {
  font-family: 'Inter', sans-serif;
  font-size: 24px;
  background-color: White;
  color: #25424C;
  padding: 5% 20%;
  gap: 3rem;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-around;
  text-align: center;
}

.eco-section img {
  transition: transform 0.5s ease;
}
.eco-section img:hover {
  transform: scale(1.05);
}

.eco-text {
  width: 50%;
}

@media (max-width: 900px) {
  .eco-section {
    padding: 5% 5%;
  }
  .eco-text {
    width: 100%;
  }
}
</style>