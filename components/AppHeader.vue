<template>
  <header>
    <div class="nav-display">
      <img
          class="logo"
          src="@/assets/images/logo-OJDeb.png"
          alt="Logo"
      />
      <div class="nav-button">
        <BaseButton class="nav-specific-button" label="Services" bgColor="#FEF0C1" />
        <BaseButton class="nav-specific-button" label="Contact" bgColor="#FEF0C1" />
      </div>
    </div>
  </header>
</template>


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

@media (max-width: 768px) {
.nav-display {
  flex-direction: column;
  gap: 1rem;
}
.nav-button {
  margin-right: 0;
  padding: 0.7rem 1rem !important;
}
}

</style>