
<template>
  <div class="hero-section">
    <img src="@/assets/images/HERO-landing.png" alt="hero-images" class="background-image" />

    <!-- Boutons en haut à droite -->
    <div class="hero-button">
      <BaseButton class="hero-specific-button" label="Services" bgColor="#B6D0C5" hoverColor="#A0BDAF"  to="/service" />
      <BaseButton class="hero-specific-button" label="Contact" bgColor="#B6D0C5" hoverColor="#A0BDAF" to="/contact" />
    </div>

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
.hero-specific-button:hover {
  background-color: #A0BDAF !important;
  opacity: 1 !important;

}

.hero-section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  color:#24424A;
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

.hero-button {
  position: absolute;
  top: 1.5rem;
  right: 4rem;
  display: flex;
  gap: 2rem;
  z-index: 3;
}

.hero-content {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  height: 100%;
  padding: 1rem;
  overflow-y: auto;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
  transition: width 0.3s ease-in-out;
}

.logo {
  height: 300px;
  margin: 5rem 0;

}

h1 {
  font-size: 2rem;
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
  transition: transform 0.5s ease;
}

button:hover {
  background-color: #A0BDAF;
  opacity: 1;
  transform: scale(1.05);
}

.hero-info {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 2rem;
  width: 100%;
  margin-bottom: 3rem;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

/* 📱 Responsive */
@media (max-width: 768px) {
.logo {
  height: 200px;
  margin: 3rem 0;
}

  .hero-info h1 {
    font-size: 1.2rem;
  }

  .hero-button {
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 0 1rem;
    box-sizing: border-box;
    position: fixed;
    top: 1rem;
    left: 0;
  }

  .hero-specific-button {
    padding: 0.7rem 1rem !important;
    background-color: #FEF0C1 !important;
  }
}


</style>