<template>
  <div class="hero-section">
    <img src="@/assets/images/HERO-landing.png" alt="hero-images" class="background-image" />
    <div class="hero-content">
      <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo" />
      <h1>Débarrassez-vous de vos encombrants avec OJ Débarras</h1>
      <div class="hero-info">
        <h1>Devis gratuit</h1>
        <h1>Intervention Rapide</h1>
      </div>
      <button>Tel: 06 23 88 18 77</button>
      <h1>HAUTE-SAVOIE - SAVOIE - AIN</h1>
    </div>
  </div>
</template>


<style scoped>

.hero-section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  height: 100vh;
  padding: 1rem;
}

.logo {
  height: 300px;
  margin-bottom: 5rem;
  margin-top: 5rem;
}

h1 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

button {
  background-color: #B6D0C5 ;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  padding: 1rem 2rem;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  border-radius: 5px;
  border: none;
  margin-bottom: 5rem;
}
button:hover {
  background-color: #A0BDAF;
  opacity: 1;
}

.hero-info {
  display: flex;
  justify-content: center;
  gap: 7rem;
  width: 100%;
  margin-bottom: 5rem;
}

</style>

