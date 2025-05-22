<template>
  <footer>
    <div class="footer-info">
      <div>
        <h4>Coordonnées</h4>
        <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo" />
        <p>
          OJ Débarras<br/>
          Annecy<br/>
          06 23 88 18 77<br/>
          ojdebarras74@exemple.com
        </p>

      </div>
      <div>
        <h4>On vous rappel</h4>
        <div>
          <ContactFormLite/>
        </div>
      </div>

      <div>
        <h4>Lieux Intervention</h4>
        <div class="localite-container">
        <p >
          Savoie <br/>
          Haute-Savoie <br/>
          Ain<br/>
        </p>
        </div>

      </div>





    </div>

    <div class="footer-signature">
      <BaseButton class="footer-specific-button" label="Devis-Gratuit" bgColor="#FEF0C1" />
    <p>&copy; 2025 OJ Débarras</p>
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
  padding: 1rem;
}

.footer-info {
  display: flex;
  justify-content: space-between;
  font-family: 'Inter', sans-serif;
  font-size: 24px;
}

.footer-info > div {
  flex: 1;
  padding: 0 1rem;
  box-sizing: border-box;
}

.localite-container{
  display: flex;
  flex-direction: column;
  justify-content: center;

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
.footer-signature > p {
  font-size: 14px;
}

.footer-specific-button {
  margin-top: 2rem;
  margin-bottom: 2rem;
}

@media (max-width: 768px) {
  .footer-info {
    flex-direction: column;
  }

  .footer-info > div {
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


</style>
