<template>
  <footer>
    <div class="footer-info">
      <div>
        <h4>Coordonnées</h4>
        <p>
          Nom: <br/>
          Adresse: <br/>
          Tel: <br/>
          Mail:
        </p>
      </div>
      <div>
        <h4>Lieu Intervention</h4>
        <p>
          Savoie <br/>
          Haute-Savoie <br/>
          Ain<br/>
        </p>
      </div>
      <div>
        <h4>A propos de nous</h4>
        <p>
          Lorem ipsum dolor sit amet,
          consectetur adipiscing elit.
          Proin in vehicula leo, porta finibus velit.
          Etiam vehicula venenatis auctor.

        </p>
      </div>
    </div>

    <div class="footer-signature">
    <p>&copy; 2025 OJ Débarras</p>
    </div>

  </footer>
</template>



<style scoped>
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
p {
  font-size: 16px;
  line-height: 2;
  display: flex;
  justify-content: flex-start;
  text-align: left;
}

.footer-signature {
  display: flex;
  justify-content: center;
  font-size: medium;
  font-family: 'Inter', sans-serif;
  color: white;
}

@media (max-width: 768px) {
  .footer-info {
    flex-direction: column;
  }

  .footer-info > div {
    margin-bottom: 1rem;
  }
}
</style>