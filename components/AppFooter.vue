<template>
  <footer>
    <div class="footer-info">
      <div>
        <h4>Coordonnées</h4>
        <div class="footer-info-container">
          <NuxtLink to="/">
            <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo" />
          </NuxtLink>
          <p>
            OJ Débarras<br />
            Annecy<br />
          </p>
          <div class="footer-info-contact">
            <a href="tel:0622822791">Tel: 06 22 82 27 91</a>
            <a href="mailto:contact.ojdebarras@gmail.com">contact.ojdebarras@gmail.com</a>
          </div>
        </div>
      </div>
      <div>
        <h4>On vous rappelle</h4>
        <div>
          <ContactFormLite />
        </div>
      </div>
      <div>
        <h4>Lieux Intervention</h4>
        <div class="localite-container">
            <p> Haute-Savoie | Savoie | Ain | Isère</p>
          <div class="footer-map-locator">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d79466.86673854114!2d6.125715272665547!3d45.88285895235016!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x478b8ffa1c0551c9%3A0x42781681620534ba!2sAnnecy!5e1!3m2!1sfr!2sfr!4v1747913175002!5m2!1sfr!2sfr"
              width="300" height="250" style="border: 1px solid rgba(255, 255, 255, 0.2); border-radius: 4px;"
              allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-signature">
      <BaseButton class="footer-specific-button" label="Devis-Gratuit" bgColor="#FEF0C1" to="/contact" />
      <div class="footer-signature-container">
        <p>&copy; 2025 OJ Débarras – Tous droits réservés</p>
        <p>Réalisation :
          <a href="https://cv-rod-fr.vercel.app/" target="_blank" rel="noopener noreferrer">R.Delory </a>
          <span class="separator">|</span>
          <a href="https://www.linkedin.com/in/eric-oriez/" target="_blank" rel="noopener noreferrer"> E.Oriez</a>
        </p>
      </div>
    </div>

  </footer>
</template>


<style scoped>
.logo {
  width: 100px;
  height: 100px;
}

footer {
  background-color: #6DA48F80;
  color: #25424C;
  text-align: center;
  padding: 1rem 1rem 0 1rem;
}

.footer-info {
  display: flex;
  justify-content: space-between;
  font-family: 'Inter', sans-serif;
  font-size: 24px;
}

.footer-info>div {
  flex: 1;
  padding: 0 1rem;
  box-sizing: border-box;
}

.footer-info-container {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 2px;
  border: 1px solid #6DA48F;
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.1),
    0 0 0 1px rgba(255, 255, 255, 0.274);
  padding: 10px;
}

.localite-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 2px;
  border: 1px solid #6DA48F;
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.1),
    0 0 0 1px rgba(255, 255, 255, 0.274);
}

.localite-container>p {
  margin: 0;
  font-size: 14px;
  font-weight: bold;

}

.footer-info-contact {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1rem;
}

.footer-info-contact>a {
  color: inherit;
  text-decoration: none;
  font-weight: bold;
}

h4 {
  font-family: 'Alkatra', sans-serif;
}

p {
  font-size: 24px;
  line-height: 2;
  display: flex;
  justify-content: center;
  text-align: center;
}

.footer-signature {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-family: 'Inter', sans-serif;
  color: white;
}

.footer-info p:first-of-type {
  font-weight: bold;
}

.footer-signature-container {
  display: flex;
  justify-content: space-around;
  gap: 1rem;
  width: 100%;
}

.footer-signature-container>p>a {
  display: inline-block;
  gap: 1rem;
  color: inherit;
  text-decoration: none;
  margin: 0 5px;
}

.footer-signature-container a:hover {
  cursor: pointer;
  text-decoration: underline;
}


.footer-signature-container .separator {
  margin: 0 5px;
  color: #999;
}

.footer-signature-container>p {
  font-size: 14px;
  margin: 0;
}

.footer-specific-button {
  margin-top: 2rem;
  margin-bottom: 2rem;
}

.footer-specific-button:hover {
  background-color: #D2B48C !important;
  opacity: 1 !important;
}

@media (max-width: 1024px) {
  .footer-info {
    flex-direction: column;
  }

  .localite-container {
    gap: 1%;
  }
}

@media (max-width: 768px) {
  .footer-info {
    flex-direction: column;

  }

  .footer-info>div {
    margin-bottom: 1rem;
  }

  .footer-info p {
    display: flex;
    justify-content: center;
    text-align: center;
  }

  .footer-specific-button {
    padding: 0.7rem 1rem !important;
  }
}

@media (max-width: 550px) {
  .footer-signature-container {
    display: flex;
    flex-direction: column;

  }
}

@media (max-width: 450px) {
  .footer-info-contact>a {

    font-size: 1.1rem;

  }
}

@media (max-width: 388px) {
  .footer-map-locator iframe {
    width: 270px;
  }
}
</style>
<script setup lang="ts">
</script>