<script setup lang="ts">
import {Send} from 'lucide-vue-next'
import {PhoneOutgoing} from 'lucide-vue-next'
import {NotebookPen} from 'lucide-vue-next'
</script>

<template>
  <div class="header-cta-band">
    <div class="header-cta-band-contact">
      <div class="header-cta-band-contact-mail">
        <Send
            color="#ff4444"
            :size="20"
        />
        <a href="mailto:o-jdebarras@hotmail.fr">o-jdebarras@hotmail.fr</a>
      </div>
      <div class="header-cta-band-contact-phone">
        <PhoneOutgoing
            color="#ff4444"
            :size="20"
        />
        <a href="tel:0623881877">Tel: 06 23 88 18 77</a>
      </div>
    </div>
    <div class="header-cta-band-button-container">
      <button class="header-cta-band-button">
        <NotebookPen />
        Devis Gratuit
      </button>
    </div>
  </div>
</template>

<style scoped>

.header-cta-band {
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: center;
  padding: 0 5%;
  font-family: 'Inter', sans-serif;
  color: #D2B48C;
  background-color: #24424A;
  height: 50px;
}

.header-cta-band-contact {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  gap: 40px;
  padding: 0 10px;
  font-family: 'Inter', sans-serif;
  color: #D2B48C;
}

.header-cta-band-contact-mail {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  gap: 5px;
  padding: 0 10px;
  font-family: 'Inter', sans-serif;
  color: #D2B48C;
}
.header-cta-band-contact-mail a,
.header-cta-band-contact-phone a {
  color: inherit;
  text-decoration: none;
}

.header-cta-band-contact-phone {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  gap: 5px;
  padding: 0 10px;
  font-family: 'Inter', sans-serif;
  color: #D2B48C;
}

.header-cta-band-button-container {
  padding: 0;
}

.header-cta-band-button {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  gap: 5px;
}

button {
  text-decoration: none;
  border: none;
  background: #ff4444;
  color: #FEF0C1;
  cursor: pointer;
  transition: transform 0.5s ease, background-color 0.3s ease;
 padding: 10px 20px;
  font-size: 18px;
  border-radius: 2px;
}

button:hover {
  background: #ff6666;
  transform: scale(1.05);
}

@media (max-width: 768px) {
  .header-cta-band-contact {
    font-size: 12px;
    gap: 10px;
    padding: 0;
  }
}

@media (max-width: 580px) {
  .header-cta-band-contact-mail {
    display: none;
  }
}
</style>