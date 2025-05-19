<template>
  <header>
    <div class="nav-display">
      <img
          class="logo"
          src="@/assets/images/logo-OJDeb.png"
          alt="Logo"
      />
      <div class="nav-button">
        <button class="nav-button-content">
          Services
        </button>
        <button class="nav-button-content">
          Contact
        </button>
      </div>
    </div>
  </header>
</template>

<script setup>
// Tu peux ajouter des méthodes ou du script ici si nécessaire
</script>

<style scoped>
header {
  background-color: #6DA48F80;
  color: white;
  padding: 1rem;
}

.logo {
  height: 5rem;
}

.nav-display {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav-button {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  margin-right: 2rem;
}

.nav-button-content {
  background-color: #FEF0C1;
  border: none;
  border-radius: 5px;
  padding: 0.7rem 4rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
}
.nav-button-content:hover {
  background-color: #FAECD6;
  opacity: 1;
}
</style>